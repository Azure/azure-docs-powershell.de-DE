---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111032"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="589ba-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="589ba-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="589ba-104">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="589ba-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-105">Az.Accounts</span></span>
* <span data-ttu-id="589ba-106">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="589ba-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="589ba-107">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="589ba-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="589ba-108">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="589ba-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-109">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-110">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="589ba-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="589ba-111">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="589ba-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="589ba-112">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="589ba-113">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="589ba-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-115">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-116">Az.IotHub</span></span>
* <span data-ttu-id="589ba-117">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="589ba-118">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="589ba-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="589ba-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="589ba-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="589ba-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="589ba-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="589ba-123">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="589ba-124">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="589ba-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="589ba-125">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="589ba-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="589ba-126">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="589ba-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="589ba-127">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="589ba-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="589ba-128">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="589ba-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="589ba-129">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="589ba-130">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="589ba-131">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="589ba-132">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="589ba-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="589ba-133">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="589ba-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="589ba-134">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="589ba-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="589ba-135">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-136">Az.Monitor</span></span>
* <span data-ttu-id="589ba-137">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="589ba-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-138">Az.Network</span></span>
* <span data-ttu-id="589ba-139">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="589ba-140">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="589ba-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="589ba-141">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="589ba-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="589ba-142">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-143">Az.Resources</span></span>
* <span data-ttu-id="589ba-144">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="589ba-145">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="589ba-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="589ba-146">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="589ba-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="589ba-147">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="589ba-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="589ba-148">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="589ba-149">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="589ba-150">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="589ba-151">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="589ba-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="589ba-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="589ba-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="589ba-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="589ba-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="589ba-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="589ba-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="589ba-155">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="589ba-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="589ba-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="589ba-157">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="589ba-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-158">Az.Sql</span></span>
* <span data-ttu-id="589ba-159">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="589ba-160">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="589ba-161">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="589ba-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="589ba-162">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="589ba-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="589ba-163">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="589ba-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="589ba-164">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="589ba-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="589ba-165">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="589ba-166">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="589ba-167">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="589ba-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-168">Az.Storage</span></span>
* <span data-ttu-id="589ba-169">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="589ba-170">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="589ba-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="589ba-171">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="589ba-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="589ba-172">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="589ba-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="589ba-173">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="589ba-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-174">Az.Websites</span></span>
* <span data-ttu-id="589ba-175">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="589ba-176">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="589ba-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="589ba-177">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="589ba-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="589ba-178">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="589ba-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="589ba-179">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="589ba-180">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="589ba-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="589ba-181">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="589ba-181">Highlights since the last major release</span></span>
* <span data-ttu-id="589ba-182">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="589ba-183">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="589ba-184">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-185">Az.Accounts</span></span>
* <span data-ttu-id="589ba-186">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-187">Az.Automation</span></span>
* <span data-ttu-id="589ba-188">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-190">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="589ba-191">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="589ba-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-192">Az.Compute</span></span>
* <span data-ttu-id="589ba-193">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="589ba-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="589ba-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-194">Az.FrontDoor</span></span>
* <span data-ttu-id="589ba-195">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="589ba-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-196">Az.IotHub</span></span>
* <span data-ttu-id="589ba-197">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="589ba-198">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="589ba-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="589ba-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="589ba-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="589ba-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="589ba-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="589ba-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-203">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-204">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-205">Az.Monitor</span></span>
* <span data-ttu-id="589ba-206">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="589ba-207">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="589ba-208">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="589ba-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-209">Az.Network</span></span>
* <span data-ttu-id="589ba-210">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="589ba-211">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="589ba-212">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="589ba-213">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="589ba-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="589ba-214">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-214">No new cmdlets are added.</span></span> <span data-ttu-id="589ba-215">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="589ba-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-217">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-218">Az.Resources</span></span>
* <span data-ttu-id="589ba-219">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="589ba-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="589ba-220">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="589ba-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="589ba-221">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="589ba-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="589ba-222">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="589ba-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="589ba-223">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="589ba-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="589ba-224">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="589ba-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="589ba-225">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="589ba-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="589ba-226">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="589ba-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-227">Az.Sql</span></span>
* <span data-ttu-id="589ba-228">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="589ba-229">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="589ba-230">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="589ba-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="589ba-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="589ba-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="589ba-232">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="589ba-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="589ba-233">Az.StorageSync</span></span>
* <span data-ttu-id="589ba-234">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="589ba-235">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="589ba-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="589ba-236">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="589ba-236">Highlights since the last major release</span></span>
* <span data-ttu-id="589ba-237">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="589ba-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="589ba-238">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-239">Az.Accounts</span></span>
* <span data-ttu-id="589ba-240">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="589ba-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="589ba-241">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="589ba-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="589ba-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-242">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-243">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="589ba-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="589ba-244">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="589ba-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="589ba-245">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="589ba-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="589ba-246">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="589ba-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-247">Az.Compute</span></span>
* <span data-ttu-id="589ba-248">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="589ba-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="589ba-249">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="589ba-250">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="589ba-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="589ba-252">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-253">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-254">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="589ba-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="589ba-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="589ba-256">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="589ba-257">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="589ba-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="589ba-258">Az.HDInsight</span></span>
* <span data-ttu-id="589ba-259">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-260">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-261">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="589ba-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-262">Az.Network</span></span>
* <span data-ttu-id="589ba-263">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="589ba-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="589ba-264">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="589ba-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="589ba-265">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="589ba-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="589ba-266">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="589ba-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="589ba-267">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="589ba-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="589ba-268">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="589ba-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="589ba-269">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="589ba-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="589ba-270">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="589ba-271">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-271">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="589ba-273">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="589ba-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="589ba-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="589ba-275">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="589ba-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="589ba-277">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="589ba-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="589ba-278">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="589ba-279">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="589ba-280">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-282">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="589ba-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="589ba-283">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-284">Az.Resources</span></span>
* <span data-ttu-id="589ba-285">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="589ba-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="589ba-286">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-287">Az.Sql</span></span>
<span data-ttu-id="589ba-288">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="589ba-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-289">Az.Storage</span></span>
* <span data-ttu-id="589ba-290">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="589ba-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="589ba-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="589ba-292">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="589ba-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="589ba-293">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-294">Az.Websites</span></span>
* <span data-ttu-id="589ba-295">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="589ba-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="589ba-296">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="589ba-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="589ba-297">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="589ba-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-298">Az.Accounts</span></span>
* <span data-ttu-id="589ba-299">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="589ba-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="589ba-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-300">Az.Cdn</span></span>
* <span data-ttu-id="589ba-301">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="589ba-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-302">Az.Compute</span></span>
* <span data-ttu-id="589ba-303">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="589ba-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="589ba-305">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="589ba-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="589ba-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="589ba-307">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="589ba-308">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="589ba-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="589ba-309">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="589ba-310">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="589ba-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="589ba-311">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="589ba-312">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="589ba-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="589ba-313">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="589ba-314">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="589ba-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="589ba-315">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="589ba-316">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="589ba-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="589ba-317">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="589ba-318">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="589ba-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="589ba-319">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="589ba-320">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="589ba-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="589ba-321">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="589ba-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="589ba-322">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="589ba-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="589ba-323">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="589ba-324">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="589ba-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-325">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-326">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="589ba-327">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="589ba-328">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="589ba-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="589ba-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="589ba-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="589ba-330">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-331">Az.EventHub</span></span>
* <span data-ttu-id="589ba-332">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="589ba-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="589ba-333">Az.HDInsight</span></span>
* <span data-ttu-id="589ba-334">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="589ba-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="589ba-335">Az.MachineLearning</span></span>
* <span data-ttu-id="589ba-336">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="589ba-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="589ba-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="589ba-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="589ba-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="589ba-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="589ba-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="589ba-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="589ba-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="589ba-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="589ba-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="589ba-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="589ba-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="589ba-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="589ba-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="589ba-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-344">Az.Network</span></span>
* <span data-ttu-id="589ba-345">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="589ba-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-347">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="589ba-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="589ba-348">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="589ba-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="589ba-349">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="589ba-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="589ba-350">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="589ba-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-351">Az.Resources</span></span>
* <span data-ttu-id="589ba-352">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-353">Az.Sql</span></span>
* <span data-ttu-id="589ba-354">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="589ba-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="589ba-355">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="589ba-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="589ba-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="589ba-357">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-358">Az.Storage</span></span>
* <span data-ttu-id="589ba-359">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="589ba-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="589ba-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="589ba-361">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="589ba-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="589ba-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="589ba-363">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="589ba-364">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-364">General</span></span>
* <span data-ttu-id="589ba-365">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-366">Az.Accounts</span></span>
* <span data-ttu-id="589ba-367">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="589ba-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="589ba-368">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="589ba-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="589ba-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="589ba-369">Az.Batch</span></span>
* <span data-ttu-id="589ba-370">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="589ba-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-371">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-372">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="589ba-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-373">Az.FrontDoor</span></span>
* <span data-ttu-id="589ba-374">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="589ba-375">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="589ba-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="589ba-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="589ba-377">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="589ba-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-378">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-379">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="589ba-380">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="589ba-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="589ba-381">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-382">Az.Monitor</span></span>
* <span data-ttu-id="589ba-383">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="589ba-384">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="589ba-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="589ba-385">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="589ba-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-386">Az.Network</span></span>
* <span data-ttu-id="589ba-387">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="589ba-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-388">Az.Resources</span></span>
* <span data-ttu-id="589ba-389">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="589ba-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="589ba-390">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="589ba-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-391">Az.Sql</span></span>
* <span data-ttu-id="589ba-392">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-393">Az.Storage</span></span>
* <span data-ttu-id="589ba-394">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="589ba-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="589ba-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="589ba-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="589ba-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="589ba-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="589ba-397">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="589ba-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="589ba-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="589ba-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="589ba-399">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="589ba-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="589ba-400">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="589ba-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="589ba-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="589ba-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="589ba-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="589ba-403">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="589ba-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="589ba-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="589ba-405">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="589ba-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="589ba-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="589ba-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="589ba-407">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="589ba-408">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="589ba-408">Highlights since the last major release</span></span>
* <span data-ttu-id="589ba-409">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="589ba-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="589ba-410">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="589ba-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-411">Az.Compute</span></span>
* <span data-ttu-id="589ba-412">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="589ba-412">VM Reapply feature</span></span>
    - <span data-ttu-id="589ba-413">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="589ba-414">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="589ba-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="589ba-415">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="589ba-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="589ba-416">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="589ba-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="589ba-417">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="589ba-418">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="589ba-419">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="589ba-420">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="589ba-421">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="589ba-422">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="589ba-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="589ba-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="589ba-424">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="589ba-425">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="589ba-425">Get the Order</span></span>
* <span data-ttu-id="589ba-426">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="589ba-427">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="589ba-427">Create new Order</span></span>
* <span data-ttu-id="589ba-428">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="589ba-429">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="589ba-429">Remove the Order</span></span>
* <span data-ttu-id="589ba-430">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="589ba-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="589ba-431">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="589ba-431">Now creates Local Share</span></span>
* <span data-ttu-id="589ba-432">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="589ba-433">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="589ba-434">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="589ba-435">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="589ba-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="589ba-436">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="589ba-437">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="589ba-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="589ba-438">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="589ba-439">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="589ba-439">Create new Triggers</span></span>
* <span data-ttu-id="589ba-440">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="589ba-441">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="589ba-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-442">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-443">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="589ba-444">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="589ba-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-446">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-447">Az.EventHub</span></span>
* <span data-ttu-id="589ba-448">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="589ba-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-449">Az.FrontDoor</span></span>
* <span data-ttu-id="589ba-450">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="589ba-451">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="589ba-452">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="589ba-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="589ba-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-454">Az.Network</span></span>
* <span data-ttu-id="589ba-455">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="589ba-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="589ba-456">Az.PrivateDns</span></span>
* <span data-ttu-id="589ba-457">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-459">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="589ba-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="589ba-460">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="589ba-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="589ba-461">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="589ba-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="589ba-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="589ba-462">Az.RedisCache</span></span>
* <span data-ttu-id="589ba-463">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="589ba-464">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="589ba-465">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-466">Az.Resources</span></span>
- <span data-ttu-id="589ba-467">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="589ba-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="589ba-468">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="589ba-469">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="589ba-470">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="589ba-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="589ba-471">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="589ba-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-472">Az.Sql</span></span>
* <span data-ttu-id="589ba-473">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="589ba-474">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="589ba-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="589ba-475">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="589ba-476">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-476">General</span></span>
* <span data-ttu-id="589ba-477">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="589ba-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-478">Az.Accounts</span></span>
* <span data-ttu-id="589ba-479">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="589ba-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="589ba-480">Az.Advisor</span></span>
* <span data-ttu-id="589ba-481">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="589ba-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="589ba-482">Az.Batch</span></span>
* <span data-ttu-id="589ba-483">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="589ba-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="589ba-484">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="589ba-485">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="589ba-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="589ba-486">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="589ba-487">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="589ba-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="589ba-488">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="589ba-489">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="589ba-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="589ba-490">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="589ba-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="589ba-491">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="589ba-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="589ba-492">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="589ba-493">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="589ba-494">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="589ba-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="589ba-495">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="589ba-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="589ba-496">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="589ba-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="589ba-497">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="589ba-498">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="589ba-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="589ba-499">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="589ba-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="589ba-500">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="589ba-501">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="589ba-502">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="589ba-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="589ba-503">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="589ba-504">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="589ba-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="589ba-505">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="589ba-506">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="589ba-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="589ba-507">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="589ba-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="589ba-508">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="589ba-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="589ba-509">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="589ba-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="589ba-510">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="589ba-511">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="589ba-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="589ba-512">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="589ba-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="589ba-513">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="589ba-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="589ba-514">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="589ba-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="589ba-515">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="589ba-516">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="589ba-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="589ba-517">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="589ba-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="589ba-518">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="589ba-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="589ba-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-519">Az.Cdn</span></span>
* <span data-ttu-id="589ba-520">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="589ba-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="589ba-521">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="589ba-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-522">Az.Compute</span></span>
* <span data-ttu-id="589ba-523">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="589ba-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="589ba-524">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="589ba-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="589ba-525">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="589ba-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="589ba-526">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="589ba-527">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="589ba-528">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="589ba-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="589ba-529">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="589ba-530">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="589ba-530">Breaking changes</span></span>
    - <span data-ttu-id="589ba-531">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="589ba-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="589ba-532">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="589ba-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-533">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-534">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-536">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="589ba-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="589ba-537">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="589ba-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="589ba-538">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="589ba-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="589ba-539">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="589ba-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="589ba-540">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="589ba-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="589ba-541">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="589ba-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="589ba-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-542">Az.FrontDoor</span></span>
* <span data-ttu-id="589ba-543">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="589ba-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="589ba-544">Az.HDInsight</span></span>
* <span data-ttu-id="589ba-545">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="589ba-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="589ba-546">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="589ba-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="589ba-547">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="589ba-548">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="589ba-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="589ba-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="589ba-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="589ba-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="589ba-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="589ba-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="589ba-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="589ba-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="589ba-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="589ba-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="589ba-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="589ba-554">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="589ba-555">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="589ba-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="589ba-556">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="589ba-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="589ba-557">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="589ba-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="589ba-558">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="589ba-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="589ba-559">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="589ba-560">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="589ba-561">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="589ba-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="589ba-562">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="589ba-563">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="589ba-564">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="589ba-565">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="589ba-566">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="589ba-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-567">Az.IotHub</span></span>
* <span data-ttu-id="589ba-568">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="589ba-568">Breaking changes:</span></span>
    - <span data-ttu-id="589ba-569">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="589ba-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="589ba-570">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="589ba-571">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="589ba-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="589ba-572">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="589ba-573">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="589ba-574">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="589ba-575">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="589ba-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="589ba-576">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="589ba-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="589ba-577">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="589ba-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="589ba-578">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="589ba-579">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="589ba-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="589ba-580">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-582">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-583">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="589ba-584">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="589ba-585">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-586">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-587">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-588">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-589">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-590">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-591">Az.Resources</span></span>
* <span data-ttu-id="589ba-592">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-593">Az.Network</span></span>
* <span data-ttu-id="589ba-594">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="589ba-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="589ba-595">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="589ba-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="589ba-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="589ba-601">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="589ba-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="589ba-602">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="589ba-602">New cmdlet:</span></span>
        - <span data-ttu-id="589ba-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="589ba-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="589ba-604">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="589ba-605">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="589ba-606">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="589ba-607">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="589ba-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="589ba-608">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="589ba-609">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="589ba-610">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="589ba-611">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-611">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="589ba-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="589ba-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="589ba-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="589ba-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="589ba-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="589ba-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="589ba-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="589ba-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="589ba-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="589ba-617">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="589ba-618">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="589ba-619">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="589ba-620">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="589ba-621">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="589ba-622">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="589ba-623">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="589ba-624">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-624">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="589ba-626">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="589ba-627">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="589ba-628">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="589ba-629">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="589ba-630">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="589ba-631">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="589ba-632">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="589ba-633">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-633">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="589ba-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="589ba-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="589ba-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="589ba-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="589ba-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="589ba-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="589ba-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="589ba-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="589ba-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="589ba-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="589ba-640">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="589ba-641">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="589ba-642">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="589ba-643">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="589ba-644">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="589ba-645">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="589ba-646">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="589ba-647">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="589ba-648">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="589ba-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="589ba-649">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="589ba-650">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="589ba-651">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-651">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="589ba-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="589ba-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="589ba-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="589ba-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="589ba-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="589ba-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="589ba-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-657">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="589ba-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-658">Az.Sql</span></span>
* <span data-ttu-id="589ba-659">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="589ba-660">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="589ba-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="589ba-661">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="589ba-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="589ba-662">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="589ba-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="589ba-663">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="589ba-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="589ba-664">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="589ba-665">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="589ba-666">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="589ba-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="589ba-667">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-668">Az.Storage</span></span>
* <span data-ttu-id="589ba-669">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="589ba-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="589ba-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="589ba-672">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="589ba-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="589ba-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="589ba-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="589ba-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="589ba-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="589ba-675">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="589ba-676">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-676">General</span></span>
* <span data-ttu-id="589ba-677">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="589ba-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-678">Az.Accounts</span></span>
* <span data-ttu-id="589ba-679">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="589ba-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-680">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-681">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="589ba-682">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="589ba-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-683">Az.Automation</span></span>
* <span data-ttu-id="589ba-684">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="589ba-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="589ba-685">Az.Batch</span></span>
* <span data-ttu-id="589ba-686">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="589ba-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-687">Az.Compute</span></span>
* <span data-ttu-id="589ba-688">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="589ba-689">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="589ba-690">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="589ba-691">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="589ba-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-692">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-693">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="589ba-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="589ba-694">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="589ba-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="589ba-695">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-697">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="589ba-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="589ba-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="589ba-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="589ba-699">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="589ba-700">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="589ba-701">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="589ba-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="589ba-702">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-703">Az.IotHub</span></span>
* <span data-ttu-id="589ba-704">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="589ba-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="589ba-705">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="589ba-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-706">Az.Monitor</span></span>
* <span data-ttu-id="589ba-707">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="589ba-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="589ba-708">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="589ba-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="589ba-709">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="589ba-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="589ba-710">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="589ba-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-711">Az.Network</span></span>
* <span data-ttu-id="589ba-712">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="589ba-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="589ba-713">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="589ba-714">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-714">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="589ba-716">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="589ba-717">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="589ba-718">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="589ba-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="589ba-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="589ba-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="589ba-722">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="589ba-723">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="589ba-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="589ba-724">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="589ba-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="589ba-725">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="589ba-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="589ba-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="589ba-726">Az.RedisCache</span></span>
* <span data-ttu-id="589ba-727">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="589ba-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-728">Az.Sql</span></span>
* <span data-ttu-id="589ba-729">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-730">Az.Storage</span></span>
* <span data-ttu-id="589ba-731">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="589ba-732">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="589ba-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="589ba-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="589ba-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="589ba-734">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="589ba-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="589ba-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="589ba-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="589ba-736">Az.StorageSync</span></span>
* <span data-ttu-id="589ba-737">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-738">Az.Websites</span></span>
* <span data-ttu-id="589ba-739">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="589ba-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="589ba-740">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="589ba-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-741">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-742">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="589ba-743">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="589ba-744">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="589ba-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-745">Az.Automation</span></span>
* <span data-ttu-id="589ba-746">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="589ba-747">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="589ba-748">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-749">Az.Compute</span></span>
* <span data-ttu-id="589ba-750">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="589ba-751">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="589ba-752">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="589ba-753">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="589ba-754">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="589ba-755">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="589ba-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="589ba-756">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="589ba-757">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="589ba-758">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-759">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-760">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="589ba-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="589ba-761">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="589ba-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="589ba-762">Az.HDInsight</span></span>
* <span data-ttu-id="589ba-763">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-764">Az.IotHub</span></span>
* <span data-ttu-id="589ba-765">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="589ba-766">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="589ba-767">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="589ba-767">New cmdlets are:</span></span>
    - <span data-ttu-id="589ba-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="589ba-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="589ba-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="589ba-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="589ba-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="589ba-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="589ba-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="589ba-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-772">Az.Monitor</span></span>
* <span data-ttu-id="589ba-773">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="589ba-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="589ba-774">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="589ba-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="589ba-775">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="589ba-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="589ba-776">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="589ba-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="589ba-777">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="589ba-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="589ba-778">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="589ba-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="589ba-779">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="589ba-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="589ba-780">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="589ba-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="589ba-781">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="589ba-782">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="589ba-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="589ba-783">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="589ba-784">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="589ba-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="589ba-785">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="589ba-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="589ba-786">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="589ba-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="589ba-787">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="589ba-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="589ba-788">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="589ba-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="589ba-789">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="589ba-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="589ba-790">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="589ba-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="589ba-791">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="589ba-792">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="589ba-792">Overall improved help files</span></span>
* <span data-ttu-id="589ba-793">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-794">Az.Network</span></span>
* <span data-ttu-id="589ba-795">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="589ba-796">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="589ba-797">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="589ba-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="589ba-798">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="589ba-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="589ba-799">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="589ba-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="589ba-800">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="589ba-801">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="589ba-802">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="589ba-803">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="589ba-804">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="589ba-805">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="589ba-806">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="589ba-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="589ba-807">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-807">New cmdlets</span></span>
        - <span data-ttu-id="589ba-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="589ba-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="589ba-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="589ba-810">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="589ba-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="589ba-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="589ba-811">New-VpnSite</span></span>
        - <span data-ttu-id="589ba-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="589ba-812">Update-VpnSite</span></span>
        - <span data-ttu-id="589ba-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-813">New-VpnConnection</span></span>
        - <span data-ttu-id="589ba-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-814">Update-VpnConnection</span></span>
* <span data-ttu-id="589ba-815">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="589ba-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-817">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="589ba-818">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-819">Az.Resources</span></span>
* <span data-ttu-id="589ba-820">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="589ba-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-822">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="589ba-823">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="589ba-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="589ba-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="589ba-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="589ba-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="589ba-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="589ba-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="589ba-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="589ba-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="589ba-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="589ba-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="589ba-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="589ba-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="589ba-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="589ba-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="589ba-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="589ba-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="589ba-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="589ba-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="589ba-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="589ba-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="589ba-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="589ba-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="589ba-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="589ba-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="589ba-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="589ba-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="589ba-837">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="589ba-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="589ba-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="589ba-838">Az.SignalR</span></span>
* <span data-ttu-id="589ba-839">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-840">Az.Sql</span></span>
* <span data-ttu-id="589ba-841">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="589ba-842">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="589ba-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="589ba-843">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="589ba-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="589ba-844">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="589ba-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="589ba-845">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="589ba-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-846">Az.Storage</span></span>
* <span data-ttu-id="589ba-847">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="589ba-848">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="589ba-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="589ba-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="589ba-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="589ba-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="589ba-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="589ba-851">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="589ba-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="589ba-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="589ba-853">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="589ba-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="589ba-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="589ba-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="589ba-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="589ba-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="589ba-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="589ba-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="589ba-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="589ba-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-858">Az.Websites</span></span>
* <span data-ttu-id="589ba-859">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="589ba-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="589ba-860">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="589ba-861">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="589ba-862">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="589ba-863">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-863">General</span></span>
* <span data-ttu-id="589ba-864">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-865">Az.Accounts</span></span>
* <span data-ttu-id="589ba-866">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="589ba-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="589ba-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="589ba-867">Az.Aks</span></span>
* <span data-ttu-id="589ba-868">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="589ba-869">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="589ba-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="589ba-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-870">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-871">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="589ba-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="589ba-872">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="589ba-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="589ba-873">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="589ba-874">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="589ba-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="589ba-875">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="589ba-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="589ba-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="589ba-876">Az.Batch</span></span>
* <span data-ttu-id="589ba-877">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="589ba-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="589ba-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-878">Az.Cdn</span></span>
* <span data-ttu-id="589ba-879">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-880">Az.Compute</span></span>
* <span data-ttu-id="589ba-881">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="589ba-882">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="589ba-883">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="589ba-884">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="589ba-885">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="589ba-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="589ba-886">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="589ba-887">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="589ba-888">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-889">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-890">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="589ba-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="589ba-891">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="589ba-892">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="589ba-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="589ba-893">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-895">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-896">Az.EventHub</span></span>
* <span data-ttu-id="589ba-897">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="589ba-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="589ba-898">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="589ba-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="589ba-899">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="589ba-900">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="589ba-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="589ba-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="589ba-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="589ba-902">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-903">Az.Monitor</span></span>
* <span data-ttu-id="589ba-904">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-905">Az.Network</span></span>
* <span data-ttu-id="589ba-906">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="589ba-907">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="589ba-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="589ba-908">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="589ba-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="589ba-909">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="589ba-910">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="589ba-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="589ba-911">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="589ba-912">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="589ba-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="589ba-914">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="589ba-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="589ba-915">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-915">Added example</span></span>
    - <span data-ttu-id="589ba-916">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="589ba-917">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="589ba-918">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-920">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-921">Az.Resources</span></span>
* <span data-ttu-id="589ba-922">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="589ba-923">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="589ba-924">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="589ba-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="589ba-925">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="589ba-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="589ba-926">Az.ServiceBus</span></span>
* <span data-ttu-id="589ba-927">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="589ba-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="589ba-928">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="589ba-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="589ba-929">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-931">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="589ba-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="589ba-932">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="589ba-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="589ba-933">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="589ba-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="589ba-934">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="589ba-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="589ba-935">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="589ba-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="589ba-936">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="589ba-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-937">Az.Sql</span></span>
* <span data-ttu-id="589ba-938">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-939">Az.Storage</span></span>
* <span data-ttu-id="589ba-940">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="589ba-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="589ba-941">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="589ba-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="589ba-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="589ba-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="589ba-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="589ba-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="589ba-944">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="589ba-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="589ba-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="589ba-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-946">Az.Websites</span></span>
* <span data-ttu-id="589ba-947">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="589ba-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="589ba-948">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-949">Az.Accounts</span></span>
* <span data-ttu-id="589ba-950">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="589ba-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="589ba-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="589ba-952">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-953">Az.Automation</span></span>
* <span data-ttu-id="589ba-954">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-956">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-957">Az.Compute</span></span>
* <span data-ttu-id="589ba-958">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="589ba-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="589ba-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="589ba-960">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="589ba-961">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="589ba-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-962">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-963">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="589ba-964">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-965">Az.EventHub</span></span>
* <span data-ttu-id="589ba-966">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="589ba-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="589ba-967">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="589ba-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-968">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-969">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="589ba-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="589ba-970">Az.LogicApp</span></span>
* <span data-ttu-id="589ba-971">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="589ba-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="589ba-972">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="589ba-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="589ba-973">Az.ManagedServices</span></span>
* <span data-ttu-id="589ba-974">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-975">Az.Network</span></span>
* <span data-ttu-id="589ba-976">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="589ba-977">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-977">New cmdlets</span></span>
        - <span data-ttu-id="589ba-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="589ba-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="589ba-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="589ba-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="589ba-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="589ba-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="589ba-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="589ba-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="589ba-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="589ba-986">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="589ba-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="589ba-987">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="589ba-988">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="589ba-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="589ba-989">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="589ba-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="589ba-990">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="589ba-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="589ba-991">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="589ba-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="589ba-992">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-992">Updated cmdlets</span></span>
        - <span data-ttu-id="589ba-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="589ba-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="589ba-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="589ba-996">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="589ba-997">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="589ba-998">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="589ba-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="589ba-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="589ba-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="589ba-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="589ba-1002">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="589ba-1003">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="589ba-1004">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="589ba-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="589ba-1006">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="589ba-1007">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1009">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="589ba-1010">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="589ba-1011">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="589ba-1012">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="589ba-1013">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="589ba-1014">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="589ba-1015">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="589ba-1016">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="589ba-1017">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="589ba-1018">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1019">Az.Resources</span></span>
- <span data-ttu-id="589ba-1020">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="589ba-1021">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="589ba-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="589ba-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="589ba-1023">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="589ba-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="589ba-1024">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1025">Az.Sql</span></span>
* <span data-ttu-id="589ba-1026">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="589ba-1027">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="589ba-1028">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1029">Az.Storage</span></span>
* <span data-ttu-id="589ba-1030">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="589ba-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="589ba-1031">Az.StorageSync</span></span>
* <span data-ttu-id="589ba-1032">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="589ba-1033">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1034">Az.Websites</span></span>
* <span data-ttu-id="589ba-1035">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="589ba-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="589ba-1036">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="589ba-1037">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="589ba-1038">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1039">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1040">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="589ba-1041">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="589ba-1042">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="589ba-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="589ba-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="589ba-1043">Az.Advisor</span></span>
* <span data-ttu-id="589ba-1044">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="589ba-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="589ba-1045">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="589ba-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="589ba-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-1047">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="589ba-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="589ba-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="589ba-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="589ba-1049">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="589ba-1050">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="589ba-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="589ba-1051">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="589ba-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="589ba-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="589ba-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="589ba-1053">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1054">Az.Automation</span></span>
* <span data-ttu-id="589ba-1055">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1056">Az.Compute</span></span>
* <span data-ttu-id="589ba-1057">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-1058">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-1059">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="589ba-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="589ba-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="589ba-1060">Az.EventGrid</span></span>
* <span data-ttu-id="589ba-1061">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1062">Az.IotHub</span></span>
* <span data-ttu-id="589ba-1063">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1064">Az.Network</span></span>
* <span data-ttu-id="589ba-1065">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="589ba-1066">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="589ba-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="589ba-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="589ba-1068">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="589ba-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="589ba-1069">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="589ba-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="589ba-1071">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1073">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="589ba-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1074">Az.Resources</span></span>
    - <span data-ttu-id="589ba-1075">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="589ba-1076">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="589ba-1077">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="589ba-1078">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="589ba-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="589ba-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="589ba-1080">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="589ba-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1081">Az.Sql</span></span>
* <span data-ttu-id="589ba-1082">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="589ba-1083">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="589ba-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="589ba-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="589ba-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="589ba-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="589ba-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="589ba-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="589ba-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="589ba-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="589ba-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="589ba-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="589ba-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="589ba-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="589ba-1090">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1091">Az.Storage</span></span>
* <span data-ttu-id="589ba-1092">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="589ba-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="589ba-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="589ba-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="589ba-1094">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="589ba-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="589ba-1095">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="589ba-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="589ba-1096">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="589ba-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="589ba-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="589ba-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="589ba-1099">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="589ba-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="589ba-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="589ba-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="589ba-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="589ba-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="589ba-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="589ba-1102">Az.StorageSync</span></span>
* <span data-ttu-id="589ba-1103">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="589ba-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="589ba-1104">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1105">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1106">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="589ba-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="589ba-1107">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="589ba-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="589ba-1108">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="589ba-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="589ba-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="589ba-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="589ba-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1111">Az.Compute</span></span>
* <span data-ttu-id="589ba-1112">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="589ba-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="589ba-1113">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="589ba-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="589ba-1114">Az.Dns</span></span>
* <span data-ttu-id="589ba-1115">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="589ba-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="589ba-1116">Az.EventGrid</span></span>
* <span data-ttu-id="589ba-1117">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="589ba-1118">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-1118">New cmdlets:</span></span>
    - <span data-ttu-id="589ba-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="589ba-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="589ba-1120">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="589ba-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="589ba-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="589ba-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="589ba-1122">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="589ba-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="589ba-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="589ba-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="589ba-1124">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="589ba-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="589ba-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="589ba-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="589ba-1126">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="589ba-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="589ba-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="589ba-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="589ba-1128">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="589ba-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="589ba-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="589ba-1130">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="589ba-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="589ba-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="589ba-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="589ba-1132">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="589ba-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="589ba-1133">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="589ba-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="589ba-1134">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="589ba-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="589ba-1135">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="589ba-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="589ba-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="589ba-1137">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="589ba-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="589ba-1138">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="589ba-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="589ba-1139">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="589ba-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="589ba-1140">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="589ba-1141">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="589ba-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="589ba-1142">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="589ba-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="589ba-1143">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="589ba-1144">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="589ba-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="589ba-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="589ba-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="589ba-1146">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="589ba-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="589ba-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="589ba-1148">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="589ba-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="589ba-1149">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="589ba-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="589ba-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="589ba-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="589ba-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="589ba-1152">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="589ba-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="589ba-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="589ba-1154">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1155">Az.Network</span></span>
* <span data-ttu-id="589ba-1156">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="589ba-1157">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1157">New cmdlets</span></span>
        - <span data-ttu-id="589ba-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="589ba-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="589ba-1159">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="589ba-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="589ba-1160">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1160">New cmdlets</span></span>
        - <span data-ttu-id="589ba-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="589ba-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="589ba-1162">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="589ba-1163">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1163">New cmdlets</span></span>
        - <span data-ttu-id="589ba-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="589ba-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="589ba-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="589ba-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="589ba-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="589ba-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="589ba-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="589ba-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="589ba-1169">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="589ba-1170">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1170">New cmdlets</span></span>
        - <span data-ttu-id="589ba-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="589ba-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="589ba-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="589ba-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="589ba-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="589ba-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="589ba-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="589ba-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="589ba-1175">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="589ba-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="589ba-1176">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="589ba-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="589ba-1177">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="589ba-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="589ba-1178">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="589ba-1179">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="589ba-1180">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="589ba-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="589ba-1181">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="589ba-1182">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="589ba-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="589ba-1183">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="589ba-1184">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="589ba-1185">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="589ba-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="589ba-1186">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="589ba-1187">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="589ba-1188">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="589ba-1189">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="589ba-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="589ba-1190">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="589ba-1191">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="589ba-1192">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="589ba-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="589ba-1193">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="589ba-1194">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="589ba-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="589ba-1195">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="589ba-1196">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="589ba-1197">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="589ba-1199">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="589ba-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1200">Az.Resources</span></span>
* <span data-ttu-id="589ba-1201">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="589ba-1202">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="589ba-1203">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="589ba-1204">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="589ba-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-1206">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="589ba-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1207">Az.Sql</span></span>
* <span data-ttu-id="589ba-1208">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="589ba-1209">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="589ba-1210">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="589ba-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="589ba-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="589ba-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="589ba-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="589ba-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="589ba-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="589ba-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="589ba-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="589ba-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="589ba-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1216">Az.Storage</span></span>
* <span data-ttu-id="589ba-1217">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="589ba-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="589ba-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="589ba-1219">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="589ba-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="589ba-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1221">Az.Websites</span></span>
* <span data-ttu-id="589ba-1222">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="589ba-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="589ba-1223">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="589ba-1224">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="589ba-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-1225">Az.Cdn</span></span>
* <span data-ttu-id="589ba-1226">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1227">Az.Compute</span></span>
* <span data-ttu-id="589ba-1228">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="589ba-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="589ba-1229">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="589ba-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1230">Az.EventHub</span></span>
* <span data-ttu-id="589ba-1231">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="589ba-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="589ba-1232">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="589ba-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1233">Az.Network</span></span>
* <span data-ttu-id="589ba-1234">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="589ba-1235">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="589ba-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="589ba-1237">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="589ba-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1239">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="589ba-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="589ba-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="589ba-1241">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="589ba-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-1243">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="589ba-1244">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1245">Az.Sql</span></span>
* <span data-ttu-id="589ba-1246">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="589ba-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="589ba-1247">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="589ba-1248">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="589ba-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="589ba-1249">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="589ba-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1250">Az.Websites</span></span>
* <span data-ttu-id="589ba-1251">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="589ba-1252">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="589ba-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-1254">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="589ba-1255">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="589ba-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="589ba-1256">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="589ba-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="589ba-1257">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="589ba-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="589ba-1258">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="589ba-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="589ba-1259">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="589ba-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="589ba-1260">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="589ba-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="589ba-1261">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="589ba-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="589ba-1262">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="589ba-1263">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="589ba-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="589ba-1264">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="589ba-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="589ba-1265">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="589ba-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="589ba-1266">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="589ba-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="589ba-1267">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="589ba-1268">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="589ba-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="589ba-1269">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="589ba-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="589ba-1270">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="589ba-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="589ba-1271">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="589ba-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="589ba-1272">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="589ba-1273">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="589ba-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="589ba-1274">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="589ba-1275">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="589ba-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="589ba-1276">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="589ba-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="589ba-1277">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="589ba-1278">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="589ba-1279">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="589ba-1280">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="589ba-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="589ba-1281">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="589ba-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="589ba-1282">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="589ba-1283">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="589ba-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="589ba-1284">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="589ba-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="589ba-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="589ba-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="589ba-1286">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="589ba-1287">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="589ba-1288">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="589ba-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="589ba-1289">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="589ba-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="589ba-1290">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="589ba-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="589ba-1291">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="589ba-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="589ba-1292">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="589ba-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="589ba-1293">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="589ba-1294">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="589ba-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="589ba-1295">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="589ba-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="589ba-1296">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="589ba-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="589ba-1297">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="589ba-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="589ba-1298">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="589ba-1299">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="589ba-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="589ba-1300">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="589ba-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="589ba-1301">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="589ba-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="589ba-1302">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="589ba-1303">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="589ba-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="589ba-1304">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="589ba-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="589ba-1305">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="589ba-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="589ba-1306">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="589ba-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="589ba-1307">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="589ba-1308">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="589ba-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="589ba-1309">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="589ba-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="589ba-1310">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="589ba-1311">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="589ba-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="589ba-1312">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="589ba-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="589ba-1313">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="589ba-1314">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="589ba-1315">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="589ba-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="589ba-1316">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="589ba-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="589ba-1317">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="589ba-1318">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="589ba-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="589ba-1319">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="589ba-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="589ba-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="589ba-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="589ba-1321">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="589ba-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="589ba-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="589ba-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="589ba-1323">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="589ba-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="589ba-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="589ba-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="589ba-1325">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="589ba-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="589ba-1326">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="589ba-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="589ba-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="589ba-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="589ba-1328">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="589ba-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="589ba-1329">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="589ba-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="589ba-1330">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="589ba-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1331">Az.Automation</span></span>
* <span data-ttu-id="589ba-1332">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="589ba-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="589ba-1333">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="589ba-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="589ba-1334">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="589ba-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="589ba-1335">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="589ba-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="589ba-1336">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="589ba-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="589ba-1337">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="589ba-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="589ba-1338">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="589ba-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1339">Az.Compute</span></span>
* <span data-ttu-id="589ba-1340">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="589ba-1341">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-1343">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="589ba-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-1344">Az.Monitor</span></span>
* <span data-ttu-id="589ba-1345">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="589ba-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1346">Az.Network</span></span>
* <span data-ttu-id="589ba-1347">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="589ba-1348">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="589ba-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="589ba-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="589ba-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="589ba-1350">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="589ba-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1351">Az.Resources</span></span>
* <span data-ttu-id="589ba-1352">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1353">Az.Sql</span></span>
* <span data-ttu-id="589ba-1354">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="589ba-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="589ba-1355">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1356">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1357">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="589ba-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-1359">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="589ba-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="589ba-1360">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="589ba-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1361">Az.Compute</span></span>
* <span data-ttu-id="589ba-1362">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="589ba-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="589ba-1363">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="589ba-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="589ba-1364">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="589ba-1365">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="589ba-1366">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="589ba-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="589ba-1367">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="589ba-1368">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="589ba-1368">Breaking changes</span></span>
    - <span data-ttu-id="589ba-1369">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="589ba-1370">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="589ba-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="589ba-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="589ba-1372">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="589ba-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="589ba-1373">Az.Dns</span></span>
* <span data-ttu-id="589ba-1374">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="589ba-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="589ba-1375">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="589ba-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="589ba-1376">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="589ba-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="589ba-1378">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="589ba-1379">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="589ba-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="589ba-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="589ba-1380">Az.HDInsight</span></span>
* <span data-ttu-id="589ba-1381">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="589ba-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="589ba-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="589ba-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="589ba-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="589ba-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="589ba-1384">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="589ba-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="589ba-1385">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="589ba-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="589ba-1386">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="589ba-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="589ba-1387">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-1388">Az.Monitor</span></span>
* <span data-ttu-id="589ba-1389">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="589ba-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="589ba-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="589ba-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="589ba-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="589ba-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="589ba-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="589ba-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="589ba-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="589ba-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="589ba-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="589ba-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="589ba-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="589ba-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="589ba-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="589ba-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="589ba-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="589ba-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="589ba-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="589ba-1401">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="589ba-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="589ba-1402">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="589ba-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1403">Az.Network</span></span>
* <span data-ttu-id="589ba-1404">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="589ba-1405">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1405">New cmdlets</span></span>
        - <span data-ttu-id="589ba-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="589ba-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="589ba-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="589ba-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="589ba-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="589ba-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="589ba-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="589ba-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="589ba-1410">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="589ba-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="589ba-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="589ba-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="589ba-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="589ba-1413">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="589ba-1414">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="589ba-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="589ba-1415">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="589ba-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="589ba-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="589ba-1417">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="589ba-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="589ba-1418">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="589ba-1419">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="589ba-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1421">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="589ba-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="589ba-1422">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="589ba-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="589ba-1423">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="589ba-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="589ba-1424">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="589ba-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="589ba-1425">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="589ba-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="589ba-1426">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="589ba-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="589ba-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="589ba-1427">Az.Relay</span></span>
* <span data-ttu-id="589ba-1428">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="589ba-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="589ba-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="589ba-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="589ba-1430">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1431">Az.Storage</span></span>
* <span data-ttu-id="589ba-1432">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="589ba-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="589ba-1433">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="589ba-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="589ba-1434">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="589ba-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="589ba-1436">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="589ba-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="589ba-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="589ba-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="589ba-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1440">Az.Websites</span></span>
* <span data-ttu-id="589ba-1441">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="589ba-1442">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="589ba-1443">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="589ba-1444">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="589ba-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="589ba-1445">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="589ba-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="589ba-1446">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="589ba-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="589ba-1447">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="589ba-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="589ba-1448">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="589ba-1449">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="589ba-1450">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="589ba-1451">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1452">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1453">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="589ba-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="589ba-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="589ba-1454">Az.Batch</span></span>
* <span data-ttu-id="589ba-1455">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="589ba-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-1456">Az.Cdn</span></span>
* <span data-ttu-id="589ba-1457">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-1459">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1460">Az.Compute</span></span>
* <span data-ttu-id="589ba-1461">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="589ba-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="589ba-1462">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="589ba-1463">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-1464">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-1465">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="589ba-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-1467">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="589ba-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="589ba-1468">Az.EventGrid</span></span>
* <span data-ttu-id="589ba-1469">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="589ba-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1470">Az.EventHub</span></span>
* <span data-ttu-id="589ba-1471">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="589ba-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="589ba-1472">Az.HDInsight</span></span>
* <span data-ttu-id="589ba-1473">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1474">Az.IotHub</span></span>
* <span data-ttu-id="589ba-1475">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-1476">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-1477">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="589ba-1478">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="589ba-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="589ba-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="589ba-1480">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="589ba-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="589ba-1481">Az.Media</span></span>
* <span data-ttu-id="589ba-1482">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-1483">Az.Monitor</span></span>
  * <span data-ttu-id="589ba-1484">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="589ba-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="589ba-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="589ba-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="589ba-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="589ba-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="589ba-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="589ba-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="589ba-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="589ba-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="589ba-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="589ba-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="589ba-1490">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1491">Az.Network</span></span>
* <span data-ttu-id="589ba-1492">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="589ba-1493">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="589ba-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="589ba-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="589ba-1495">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="589ba-1497">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="589ba-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="589ba-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="589ba-1499">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1501">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="589ba-1502">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="589ba-1503">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="589ba-1504">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="589ba-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="589ba-1505">Az.RedisCache</span></span>
* <span data-ttu-id="589ba-1506">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1507">Az.Resources</span></span>
* <span data-ttu-id="589ba-1508">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1509">Az.Sql</span></span>
* <span data-ttu-id="589ba-1510">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="589ba-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="589ba-1511">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="589ba-1512">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="589ba-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="589ba-1513">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="589ba-1514">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="589ba-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="589ba-1515">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="589ba-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="589ba-1516">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1517">Az.Websites</span></span>
* <span data-ttu-id="589ba-1518">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="589ba-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="589ba-1519">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="589ba-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="589ba-1520">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="589ba-1521">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="589ba-1522">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="589ba-1523">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="589ba-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="589ba-1524">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="589ba-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="589ba-1525">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="589ba-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="589ba-1526">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="589ba-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="589ba-1527">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="589ba-1528">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="589ba-1529">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="589ba-1530">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="589ba-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1531">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1532">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="589ba-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="589ba-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="589ba-1534">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="589ba-1535">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1536">Az.Automation</span></span>
* <span data-ttu-id="589ba-1537">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="589ba-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="589ba-1538">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="589ba-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="589ba-1539">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="589ba-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1540">Az.Compute</span></span>
* <span data-ttu-id="589ba-1541">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="589ba-1542">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="589ba-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="589ba-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="589ba-1544">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="589ba-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-1545">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-1546">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="589ba-1547">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1548">Az.Resources</span></span>
* <span data-ttu-id="589ba-1549">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="589ba-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="589ba-1550">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="589ba-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="589ba-1551">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="589ba-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="589ba-1552">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="589ba-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="589ba-1553">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="589ba-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="589ba-1554">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="589ba-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1555">Az.Sql</span></span>
* <span data-ttu-id="589ba-1556">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="589ba-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1557">Az.Storage</span></span>
* <span data-ttu-id="589ba-1558">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="589ba-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="589ba-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="589ba-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="589ba-1560">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="589ba-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="589ba-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="589ba-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="589ba-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="589ba-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="589ba-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="589ba-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="589ba-1565">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="589ba-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="589ba-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="589ba-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="589ba-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="589ba-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="589ba-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="589ba-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="589ba-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="589ba-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="589ba-1570">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="589ba-1571">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="589ba-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="589ba-1572">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="589ba-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="589ba-1573">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="589ba-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="589ba-1574">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="589ba-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="589ba-1575">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="589ba-1576">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="589ba-1577">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="589ba-1578">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1579">Az.Automation</span></span>
* <span data-ttu-id="589ba-1580">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="589ba-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="589ba-1581">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="589ba-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="589ba-1582">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="589ba-1582">Pre-Post script</span></span>
    * <span data-ttu-id="589ba-1583">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="589ba-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1584">Az.Compute</span></span>
* <span data-ttu-id="589ba-1585">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="589ba-1586">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-1587">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-1588">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1589">Az.Network</span></span>
* <span data-ttu-id="589ba-1590">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="589ba-1591">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1593">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="589ba-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="589ba-1594">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1595">Az.Resources</span></span>
* <span data-ttu-id="589ba-1596">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="589ba-1597">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="589ba-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1598">Az.Sql</span></span>
* <span data-ttu-id="589ba-1599">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1600">Az.Storage</span></span>
* <span data-ttu-id="589ba-1601">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="589ba-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="589ba-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="589ba-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="589ba-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="589ba-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="589ba-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="589ba-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="589ba-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="589ba-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1608">Az.Websites</span></span>
* <span data-ttu-id="589ba-1609">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="589ba-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="589ba-1610">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1611">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1612">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="589ba-1613">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1614">Az.Automation</span></span>
* <span data-ttu-id="589ba-1615">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="589ba-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="589ba-1616">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="589ba-1617">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="589ba-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="589ba-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-1618">Az.Cdn</span></span>
* <span data-ttu-id="589ba-1619">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="589ba-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1620">Az.Compute</span></span>
* <span data-ttu-id="589ba-1621">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-1622">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-1623">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="589ba-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="589ba-1624">Az.LogicApp</span></span>
* <span data-ttu-id="589ba-1625">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="589ba-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1626">Az.Network</span></span>
* <span data-ttu-id="589ba-1627">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1629">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="589ba-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="589ba-1630">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="589ba-1630">SDK Update</span></span>
* <span data-ttu-id="589ba-1631">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="589ba-1632">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1633">Az.Resources</span></span>
* <span data-ttu-id="589ba-1634">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="589ba-1635">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="589ba-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="589ba-1636">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="589ba-1637">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="589ba-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="589ba-1638">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="589ba-1639">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="589ba-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1640">Az.Sql</span></span>
* <span data-ttu-id="589ba-1641">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="589ba-1642">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1643">Az.Storage</span></span>
* <span data-ttu-id="589ba-1644">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="589ba-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="589ba-1645">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="589ba-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="589ba-1647">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1648">Az.Automation</span></span>
* <span data-ttu-id="589ba-1649">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="589ba-1650">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="589ba-1651">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="589ba-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-1653">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1654">Az.Compute</span></span>
* <span data-ttu-id="589ba-1655">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="589ba-1656">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="589ba-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="589ba-1657">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="589ba-1658">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="589ba-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-1660">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="589ba-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1661">Az.EventHub</span></span>
* <span data-ttu-id="589ba-1662">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-1663">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-1664">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="589ba-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="589ba-1665">Az.LogicApp</span></span>
* <span data-ttu-id="589ba-1666">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="589ba-1667">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="589ba-1668">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="589ba-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="589ba-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="589ba-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="589ba-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="589ba-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="589ba-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="589ba-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="589ba-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="589ba-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="589ba-1673">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="589ba-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="589ba-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="589ba-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="589ba-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="589ba-1678">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="589ba-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-1679">Az.Monitor</span></span>
* <span data-ttu-id="589ba-1680">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1681">Az.Network</span></span>
* <span data-ttu-id="589ba-1682">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="589ba-1684">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="589ba-1685">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="589ba-1686">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="589ba-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1687">Az.Resources</span></span>
* <span data-ttu-id="589ba-1688">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="589ba-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="589ba-1689">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="589ba-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="589ba-1690">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="589ba-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="589ba-1691">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="589ba-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1692">Az.Sql</span></span>
* <span data-ttu-id="589ba-1693">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="589ba-1694">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="589ba-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1695">Az.Websites</span></span>
* <span data-ttu-id="589ba-1696">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="589ba-1697">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1698">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1699">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="589ba-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="589ba-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="589ba-1701">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="589ba-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1702">Az.Compute</span></span>
* <span data-ttu-id="589ba-1703">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="589ba-1704">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="589ba-1705">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="589ba-1707">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="589ba-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1708">Az.Resources</span></span>
* <span data-ttu-id="589ba-1709">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="589ba-1710">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="589ba-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="589ba-1711">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="589ba-1712">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="589ba-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1713">Az.Sql</span></span>
* <span data-ttu-id="589ba-1714">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="589ba-1715">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="589ba-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="589ba-1716">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="589ba-1717">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1718">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1719">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="589ba-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="589ba-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="589ba-1721">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="589ba-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="589ba-1723">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="589ba-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="589ba-1724">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1725">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1726">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="589ba-1727">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="589ba-1728">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="589ba-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="589ba-1729">Az.Aks</span></span>
* <span data-ttu-id="589ba-1730">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="589ba-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1731">Az.Automation</span></span>
* <span data-ttu-id="589ba-1732">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="589ba-1733">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="589ba-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="589ba-1734">Az.Cdn</span></span>
* <span data-ttu-id="589ba-1735">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1736">Az.Compute</span></span>
* <span data-ttu-id="589ba-1737">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="589ba-1738">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="589ba-1739">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="589ba-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="589ba-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="589ba-1741">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="589ba-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="589ba-1742">Az.DataFactory</span></span>
* <span data-ttu-id="589ba-1743">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-1745">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="589ba-1746">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="589ba-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="589ba-1747">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1748">Az.IotHub</span></span>
* <span data-ttu-id="589ba-1749">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="589ba-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-1750">Az.KeyVault</span></span>
* <span data-ttu-id="589ba-1751">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1752">Az.Network</span></span>
* <span data-ttu-id="589ba-1753">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1754">Az.Resources</span></span>
* <span data-ttu-id="589ba-1755">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="589ba-1756">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="589ba-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="589ba-1757">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="589ba-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="589ba-1758">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="589ba-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="589ba-1759">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="589ba-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="589ba-1760">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="589ba-1761">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="589ba-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-1763">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="589ba-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="589ba-1764">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1764">Fix some error messages.</span></span>
* <span data-ttu-id="589ba-1765">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="589ba-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="589ba-1766">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="589ba-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="589ba-1767">Az.SignalR</span></span>
* <span data-ttu-id="589ba-1768">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1769">Az.Sql</span></span>
* <span data-ttu-id="589ba-1770">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="589ba-1771">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="589ba-1772">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="589ba-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="589ba-1773">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="589ba-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1774">Az.Storage</span></span>
* <span data-ttu-id="589ba-1775">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="589ba-1776">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="589ba-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="589ba-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="589ba-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="589ba-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="589ba-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="589ba-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="589ba-1780">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1781">Az.Websites</span></span>
* <span data-ttu-id="589ba-1782">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="589ba-1783">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="589ba-1784">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="589ba-1785">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="589ba-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="589ba-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1786">Az.Accounts</span></span>
* <span data-ttu-id="589ba-1787">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1788">Az.Compute</span></span>
* <span data-ttu-id="589ba-1789">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="589ba-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="589ba-1790">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="589ba-1791">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-1793">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="589ba-1794">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="589ba-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="589ba-1795">Az.EventGrid</span></span>
* <span data-ttu-id="589ba-1796">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="589ba-1797">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="589ba-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="589ba-1798">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="589ba-1799">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="589ba-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="589ba-1800">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="589ba-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="589ba-1801">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="589ba-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="589ba-1802">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="589ba-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="589ba-1803">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="589ba-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="589ba-1804">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="589ba-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="589ba-1805">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="589ba-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="589ba-1806">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="589ba-1807">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="589ba-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="589ba-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="589ba-1808">Az.IotHub</span></span>
* <span data-ttu-id="589ba-1809">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="589ba-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="589ba-1810">Az.LogicApp</span></span>
* <span data-ttu-id="589ba-1811">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="589ba-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1812">Az.Resources</span></span>
* <span data-ttu-id="589ba-1813">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="589ba-1814">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="589ba-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="589ba-1815">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="589ba-1816">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="589ba-1817">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="589ba-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="589ba-1818">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="589ba-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="589ba-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="589ba-1819">Az.SignalR</span></span>
* <span data-ttu-id="589ba-1820">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1821">Az.Sql</span></span>
* <span data-ttu-id="589ba-1822">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="589ba-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1823">Az.Storage</span></span>
* <span data-ttu-id="589ba-1824">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="589ba-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="589ba-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="589ba-1826">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="589ba-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="589ba-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="589ba-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1828">Az.Websites</span></span>
* <span data-ttu-id="589ba-1829">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="589ba-1830">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="589ba-1831">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="589ba-1832">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-1832">General</span></span>

- <span data-ttu-id="589ba-1833">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="589ba-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="589ba-1834">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="589ba-1834">Online help for each module</span></span>
- <span data-ttu-id="589ba-1835">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="589ba-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="589ba-1836">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="589ba-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="589ba-1837">Az.Accounts</span></span>
- <span data-ttu-id="589ba-1838">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="589ba-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="589ba-1839">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="589ba-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="589ba-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="589ba-1841">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="589ba-1841">Fixes for #7002</span></span>
- <span data-ttu-id="589ba-1842">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="589ba-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="589ba-1843">Az.Batch</span></span>
- <span data-ttu-id="589ba-1844">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="589ba-1845">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="589ba-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="589ba-1846">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="589ba-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="589ba-1847">Az.Billing</span></span>
- <span data-ttu-id="589ba-1848">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="589ba-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="589ba-1850">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="589ba-1851">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="589ba-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="589ba-1853">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="589ba-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="589ba-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="589ba-1855">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="589ba-1857">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="589ba-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="589ba-1858">Az.Monitor</span></span>
- <span data-ttu-id="589ba-1859">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="589ba-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="589ba-1860">Az.KeyVault</span></span>
- <span data-ttu-id="589ba-1861">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="589ba-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="589ba-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="589ba-1863">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="589ba-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="589ba-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="589ba-1864">Az.Media</span></span>
- <span data-ttu-id="589ba-1865">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="589ba-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="589ba-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1866">Az.Network</span></span>
<span data-ttu-id="589ba-1867">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="589ba-1868">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="589ba-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="589ba-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="589ba-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="589ba-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="589ba-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589ba-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="589ba-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="589ba-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="589ba-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="589ba-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="589ba-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="589ba-1877">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="589ba-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="589ba-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="589ba-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="589ba-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="589ba-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="589ba-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="589ba-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="589ba-1883">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="589ba-1884">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="589ba-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="589ba-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="589ba-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="589ba-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="589ba-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="589ba-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="589ba-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="589ba-1888">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="589ba-1889">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="589ba-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="589ba-1891">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="589ba-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="589ba-1892">Az.Profile</span></span>
- <span data-ttu-id="589ba-1893">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="589ba-1895">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="589ba-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1896">Az.Resources</span></span>
- <span data-ttu-id="589ba-1897">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="589ba-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="589ba-1899">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="589ba-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="589ba-1900">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="589ba-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="589ba-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="589ba-1902">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="589ba-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="589ba-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1903">Az.Sql</span></span>
- <span data-ttu-id="589ba-1904">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="589ba-1905">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="589ba-1906">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="589ba-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1907">Az.Storage</span></span>
- <span data-ttu-id="589ba-1908">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="589ba-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1909">Az.Websites</span></span>
- <span data-ttu-id="589ba-1910">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="589ba-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="589ba-1911">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="589ba-1912">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-1912">General</span></span>

* <span data-ttu-id="589ba-1913">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="589ba-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="589ba-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1914">Az.Compute</span></span>

* <span data-ttu-id="589ba-1915">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="589ba-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="589ba-1917">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="589ba-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="589ba-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="589ba-1919">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="589ba-1920">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="589ba-1921">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="589ba-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="589ba-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="589ba-1923">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="589ba-1924">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="589ba-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="589ba-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1925">Az.Resources</span></span>

* <span data-ttu-id="589ba-1926">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="589ba-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="589ba-1927">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="589ba-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="589ba-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1928">Az.Sql</span></span>

* <span data-ttu-id="589ba-1929">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="589ba-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="589ba-1930">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="589ba-1931">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="589ba-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="589ba-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-1932">Az.Storage</span></span>

* <span data-ttu-id="589ba-1933">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="589ba-1934">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="589ba-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="589ba-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="589ba-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="589ba-1936">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="589ba-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="589ba-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="589ba-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="589ba-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="589ba-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-1939">Az.Websites</span></span>

* <span data-ttu-id="589ba-1940">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="589ba-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="589ba-1941">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="589ba-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="589ba-1942">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="589ba-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="589ba-1943">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="589ba-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="589ba-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="589ba-1945">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="589ba-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="589ba-1946">Az.Automation</span></span>
* <span data-ttu-id="589ba-1947">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="589ba-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="589ba-1948">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="589ba-1949">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="589ba-1950">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="589ba-1951">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="589ba-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-1952">Az.Compute</span></span>
* <span data-ttu-id="589ba-1953">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="589ba-1954">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="589ba-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="589ba-1956">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="589ba-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="589ba-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="589ba-1958">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="589ba-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-1959">Az.Network</span></span>
* <span data-ttu-id="589ba-1960">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="589ba-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="589ba-1961">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="589ba-1962">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="589ba-1963">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="589ba-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="589ba-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="589ba-1965">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="589ba-1966">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="589ba-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="589ba-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="589ba-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="589ba-1968">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="589ba-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="589ba-1969">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="589ba-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="589ba-1970">Az.Relay</span></span>
* <span data-ttu-id="589ba-1971">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="589ba-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="589ba-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-1972">Az.Resources</span></span>
* <span data-ttu-id="589ba-1973">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="589ba-1974">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="589ba-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="589ba-1975">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="589ba-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="589ba-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-1977">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="589ba-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-1978">Az.Sql</span></span>
* <span data-ttu-id="589ba-1979">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="589ba-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="589ba-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="589ba-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="589ba-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="589ba-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="589ba-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="589ba-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="589ba-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="589ba-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="589ba-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="589ba-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="589ba-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="589ba-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="589ba-1988">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="589ba-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="589ba-1989">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="589ba-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="589ba-1990">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="589ba-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="589ba-1991">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="589ba-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="589ba-1992">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="589ba-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="589ba-1993">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="589ba-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="589ba-1994">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="589ba-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="589ba-1995">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="589ba-1996">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="589ba-1997">Allgemein</span><span class="sxs-lookup"><span data-stu-id="589ba-1997">General</span></span>
* <span data-ttu-id="589ba-1998">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="589ba-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="589ba-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="589ba-1999">Az.Profile</span></span>
* <span data-ttu-id="589ba-2000">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="589ba-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="589ba-2001">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="589ba-2002">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="589ba-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="589ba-2003">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="589ba-2004">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="589ba-2005">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="589ba-2006">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="589ba-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-2008">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-2009">Az.Compute</span></span>
* <span data-ttu-id="589ba-2010">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="589ba-2011">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="589ba-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="589ba-2012">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="589ba-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-2014">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="589ba-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="589ba-2015">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="589ba-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="589ba-2016">Az.Insights</span></span>
* <span data-ttu-id="589ba-2017">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="589ba-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="589ba-2018">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="589ba-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="589ba-2019">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="589ba-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="589ba-2020">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-2021">Az.Network</span></span>
* <span data-ttu-id="589ba-2022">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="589ba-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="589ba-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="589ba-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="589ba-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="589ba-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="589ba-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="589ba-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="589ba-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="589ba-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="589ba-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="589ba-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="589ba-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="589ba-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="589ba-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="589ba-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="589ba-2030">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-2031">Az.Resources</span></span>
* <span data-ttu-id="589ba-2032">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="589ba-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="589ba-2033">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="589ba-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="589ba-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="589ba-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="589ba-2035">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="589ba-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="589ba-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="589ba-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="589ba-2037">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="589ba-2038">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="589ba-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="589ba-2039">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="589ba-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="589ba-2040">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="589ba-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="589ba-2041">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="589ba-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="589ba-2042">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="589ba-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="589ba-2043">Az.Profile</span></span>
* <span data-ttu-id="589ba-2044">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="589ba-2045">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="589ba-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-2046">Az.Compute</span></span>
* <span data-ttu-id="589ba-2047">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="589ba-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="589ba-2048">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="589ba-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="589ba-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="589ba-2050">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="589ba-2051">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="589ba-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="589ba-2052">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="589ba-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="589ba-2053">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="589ba-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="589ba-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="589ba-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-2055">Az.Network</span></span>
* <span data-ttu-id="589ba-2056">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="589ba-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="589ba-2057">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-2058">Az.Resources</span></span>
* <span data-ttu-id="589ba-2059">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="589ba-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="589ba-2060">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="589ba-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="589ba-2061">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="589ba-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="589ba-2062">Azure.Storage</span></span>
* <span data-ttu-id="589ba-2063">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="589ba-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="589ba-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="589ba-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="589ba-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="589ba-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="589ba-2066">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="589ba-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="589ba-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="589ba-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="589ba-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="589ba-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="589ba-2069">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="589ba-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="589ba-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="589ba-2070">Az.Compute</span></span>
* <span data-ttu-id="589ba-2071">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="589ba-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="589ba-2072">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="589ba-2073">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="589ba-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="589ba-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="589ba-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="589ba-2075">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="589ba-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="589ba-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="589ba-2076">Az.Network</span></span>
* <span data-ttu-id="589ba-2077">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="589ba-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="589ba-2078">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2078">new cmdlets added</span></span>
    - <span data-ttu-id="589ba-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="589ba-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="589ba-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="589ba-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="589ba-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="589ba-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="589ba-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="589ba-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="589ba-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="589ba-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="589ba-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="589ba-2085">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="589ba-2086">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="589ba-2087">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="589ba-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="589ba-2088">Az.RedisCache</span></span>
* <span data-ttu-id="589ba-2089">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="589ba-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="589ba-2090">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="589ba-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="589ba-2091">Az.Resources</span></span>
* <span data-ttu-id="589ba-2092">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="589ba-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="589ba-2093">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="589ba-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="589ba-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="589ba-2094">Az.Sql</span></span>
* <span data-ttu-id="589ba-2095">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="589ba-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="589ba-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="589ba-2096">Az.Websites</span></span>
* <span data-ttu-id="589ba-2097">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="589ba-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="589ba-2098">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="589ba-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="589ba-2099">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="589ba-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="589ba-2100">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="589ba-2100">Initial Release</span></span>
