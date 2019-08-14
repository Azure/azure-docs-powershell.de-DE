---
ms.openlocfilehash: faf9313d642a3ca45731f4527aafdfd7f5096a78
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861282"
---
## <a name="180---april-2019"></a><span data-ttu-id="aece4-101">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aece4-102">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="aece4-102">Highlights since the last major release</span></span>
* <span data-ttu-id="aece4-103">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="aece4-103">General availability of `Az` module</span></span>
* <span data-ttu-id="aece4-104">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="aece4-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aece4-105">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="aece4-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aece4-106">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aece4-107">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aece4-108">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aece4-109">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aece4-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-110">Az.Accounts</span></span>
* <span data-ttu-id="aece4-111">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="aece4-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="aece4-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aece4-112">Az.Batch</span></span>
* <span data-ttu-id="aece4-113">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aece4-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aece4-114">Az.Cdn</span></span>
* <span data-ttu-id="aece4-115">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aece4-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aece4-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="aece4-117">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-118">Az.Compute</span></span>
* <span data-ttu-id="aece4-119">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="aece4-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="aece4-120">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aece4-121">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aece4-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aece4-122">Az.DataFactory</span></span>
* <span data-ttu-id="aece4-123">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="aece4-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aece4-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="aece4-125">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aece4-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aece4-126">Az.EventGrid</span></span>
* <span data-ttu-id="aece4-127">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aece4-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aece4-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aece4-128">Az.EventHub</span></span>
* <span data-ttu-id="aece4-129">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="aece4-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="aece4-130">Az.HDInsight</span></span>
* <span data-ttu-id="aece4-131">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aece4-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aece4-132">Az.IotHub</span></span>
* <span data-ttu-id="aece4-133">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aece4-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aece4-134">Az.KeyVault</span></span>
* <span data-ttu-id="aece4-135">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aece4-136">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="aece4-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aece4-137">Az.MachineLearning</span></span>
* <span data-ttu-id="aece4-138">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="aece4-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aece4-139">Az.Media</span></span>
* <span data-ttu-id="aece4-140">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aece4-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aece4-141">Az.Monitor</span></span>
  * <span data-ttu-id="aece4-142">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="aece4-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="aece4-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="aece4-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="aece4-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="aece4-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="aece4-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aece4-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="aece4-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aece4-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="aece4-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aece4-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="aece4-148">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-149">Az.Network</span></span>
* <span data-ttu-id="aece4-150">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aece4-151">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="aece4-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="aece4-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="aece4-153">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aece4-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aece4-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="aece4-155">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="aece4-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="aece4-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="aece4-157">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="aece4-159">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aece4-160">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="aece4-161">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="aece4-162">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aece4-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aece4-163">Az.RedisCache</span></span>
* <span data-ttu-id="aece4-164">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-165">Az.Resources</span></span>
* <span data-ttu-id="aece4-166">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-167">Az.Sql</span></span>
* <span data-ttu-id="aece4-168">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="aece4-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="aece4-169">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aece4-170">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="aece4-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="aece4-171">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="aece4-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="aece4-172">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="aece4-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="aece4-173">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="aece4-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="aece4-174">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aece4-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-175">Az.Websites</span></span>
* <span data-ttu-id="aece4-176">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="aece4-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="aece4-177">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aece4-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aece4-178">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="aece4-179">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="aece4-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="aece4-180">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aece4-181">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="aece4-181">Highlights since the last major release</span></span>
* <span data-ttu-id="aece4-182">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="aece4-182">General availability of `Az` module</span></span>
* <span data-ttu-id="aece4-183">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="aece4-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aece4-184">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="aece4-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aece4-185">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aece4-186">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aece4-187">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aece4-188">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aece4-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-189">Az.Accounts</span></span>
* <span data-ttu-id="aece4-190">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="aece4-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aece4-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aece4-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="aece4-192">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="aece4-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="aece4-193">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="aece4-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aece4-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aece4-194">Az.Automation</span></span>
* <span data-ttu-id="aece4-195">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="aece4-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="aece4-196">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="aece4-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="aece4-197">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="aece4-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-198">Az.Compute</span></span>
* <span data-ttu-id="aece4-199">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="aece4-200">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="aece4-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="aece4-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="aece4-202">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="aece4-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aece4-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aece4-203">Az.DataFactory</span></span>
* <span data-ttu-id="aece4-204">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="aece4-205">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-206">Az.Resources</span></span>
* <span data-ttu-id="aece4-207">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="aece4-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="aece4-208">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="aece4-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="aece4-209">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="aece4-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="aece4-210">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aece4-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="aece4-211">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="aece4-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="aece4-212">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aece4-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-213">Az.Sql</span></span>
* <span data-ttu-id="aece4-214">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="aece4-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aece4-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-215">Az.Storage</span></span>
* <span data-ttu-id="aece4-216">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="aece4-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="aece4-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aece4-217">New-AzStorageContext</span></span>
* <span data-ttu-id="aece4-218">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="aece4-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="aece4-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aece4-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aece4-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aece4-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aece4-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aece4-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="aece4-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aece4-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="aece4-223">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="aece4-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="aece4-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aece4-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aece4-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aece4-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aece4-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aece4-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="aece4-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aece4-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="aece4-228">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aece4-229">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="aece4-229">Highlights since the last major release</span></span>
* <span data-ttu-id="aece4-230">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="aece4-230">General availability of `Az` module</span></span>
* <span data-ttu-id="aece4-231">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="aece4-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aece4-232">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="aece4-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aece4-233">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aece4-234">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aece4-235">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aece4-236">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aece4-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aece4-237">Az.Automation</span></span>
* <span data-ttu-id="aece4-238">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="aece4-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="aece4-239">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="aece4-239">Dynamic grouping</span></span>
    * <span data-ttu-id="aece4-240">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="aece4-240">Pre-Post script</span></span>
    * <span data-ttu-id="aece4-241">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="aece4-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-242">Az.Compute</span></span>
* <span data-ttu-id="aece4-243">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="aece4-244">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aece4-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aece4-245">Az.KeyVault</span></span>
* <span data-ttu-id="aece4-246">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-247">Az.Network</span></span>
* <span data-ttu-id="aece4-248">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="aece4-249">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="aece4-251">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="aece4-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="aece4-252">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-253">Az.Resources</span></span>
* <span data-ttu-id="aece4-254">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="aece4-255">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aece4-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-256">Az.Sql</span></span>
* <span data-ttu-id="aece4-257">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aece4-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aece4-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-258">Az.Storage</span></span>
* <span data-ttu-id="aece4-259">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="aece4-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aece4-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aece4-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aece4-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aece4-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aece4-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aece4-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="aece4-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="aece4-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="aece4-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="aece4-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="aece4-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aece4-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-266">Az.Websites</span></span>
* <span data-ttu-id="aece4-267">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="aece4-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="aece4-268">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aece4-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-269">Az.Accounts</span></span>
* <span data-ttu-id="aece4-270">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aece4-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="aece4-271">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aece4-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aece4-272">Az.Automation</span></span>
* <span data-ttu-id="aece4-273">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="aece4-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="aece4-274">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="aece4-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="aece4-275">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aece4-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aece4-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aece4-276">Az.Cdn</span></span>
* <span data-ttu-id="aece4-277">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="aece4-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-278">Az.Compute</span></span>
* <span data-ttu-id="aece4-279">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aece4-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aece4-280">Az.DataFactory</span></span>
* <span data-ttu-id="aece4-281">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aece4-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aece4-282">Az.LogicApp</span></span>
* <span data-ttu-id="aece4-283">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="aece4-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-284">Az.Network</span></span>
* <span data-ttu-id="aece4-285">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="aece4-287">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="aece4-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="aece4-288">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="aece4-288">SDK Update</span></span>
* <span data-ttu-id="aece4-289">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="aece4-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="aece4-290">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-291">Az.Resources</span></span>
* <span data-ttu-id="aece4-292">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="aece4-293">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="aece4-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="aece4-294">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="aece4-295">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="aece4-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="aece4-296">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="aece4-297">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="aece4-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-298">Az.Sql</span></span>
* <span data-ttu-id="aece4-299">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="aece4-300">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aece4-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-301">Az.Storage</span></span>
* <span data-ttu-id="aece4-302">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aece4-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="aece4-303">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="aece4-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aece4-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="aece4-305">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="aece4-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aece4-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aece4-306">Az.Automation</span></span>
* <span data-ttu-id="aece4-307">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="aece4-308">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="aece4-309">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="aece4-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aece4-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aece4-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="aece4-311">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aece4-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-312">Az.Compute</span></span>
* <span data-ttu-id="aece4-313">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="aece4-314">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="aece4-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="aece4-315">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="aece4-316">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="aece4-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aece4-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="aece4-318">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aece4-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aece4-319">Az.EventHub</span></span>
* <span data-ttu-id="aece4-320">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="aece4-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aece4-321">Az.KeyVault</span></span>
* <span data-ttu-id="aece4-322">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aece4-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aece4-323">Az.LogicApp</span></span>
* <span data-ttu-id="aece4-324">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="aece4-325">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="aece4-326">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="aece4-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="aece4-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aece4-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aece4-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aece4-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aece4-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aece4-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aece4-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aece4-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="aece4-331">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="aece4-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aece4-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aece4-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aece4-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="aece4-336">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aece4-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aece4-337">Az.Monitor</span></span>
* <span data-ttu-id="aece4-338">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-339">Az.Network</span></span>
* <span data-ttu-id="aece4-340">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aece4-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aece4-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="aece4-342">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="aece4-343">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="aece4-344">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="aece4-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="aece4-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-345">Az.Resources</span></span>
* <span data-ttu-id="aece4-346">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aece4-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aece4-347">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aece4-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="aece4-348">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="aece4-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="aece4-349">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="aece4-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-350">Az.Sql</span></span>
* <span data-ttu-id="aece4-351">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="aece4-352">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="aece4-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aece4-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-353">Az.Websites</span></span>
* <span data-ttu-id="aece4-354">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="aece4-355">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aece4-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-356">Az.Accounts</span></span>
* <span data-ttu-id="aece4-357">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="aece4-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aece4-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aece4-358">Az.AnalysisServices</span></span>
<span data-ttu-id="aece4-359">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="aece4-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-360">Az.Compute</span></span>
* <span data-ttu-id="aece4-361">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="aece4-362">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="aece4-363">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-364">Az.RecoveryServices</span></span>
<span data-ttu-id="aece4-365">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="aece4-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-366">Az.Resources</span></span>
* <span data-ttu-id="aece4-367">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="aece4-368">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aece4-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aece4-369">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="aece4-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="aece4-370">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aece4-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-371">Az.Sql</span></span>
* <span data-ttu-id="aece4-372">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="aece4-373">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="aece4-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="aece4-374">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="aece4-375">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aece4-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-376">Az.Accounts</span></span>
* <span data-ttu-id="aece4-377">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="aece4-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aece4-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aece4-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="aece4-379">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="aece4-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="aece4-381">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="aece4-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="aece4-382">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aece4-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-383">Az.Accounts</span></span>
* <span data-ttu-id="aece4-384">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aece4-385">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aece4-386">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="aece4-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="aece4-387">Az.Aks</span></span>
* <span data-ttu-id="aece4-388">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aece4-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aece4-389">Az.Automation</span></span>
* <span data-ttu-id="aece4-390">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="aece4-391">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aece4-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aece4-392">Az.Cdn</span></span>
* <span data-ttu-id="aece4-393">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-394">Az.Compute</span></span>
* <span data-ttu-id="aece4-395">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="aece4-396">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="aece4-397">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="aece4-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aece4-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="aece4-399">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aece4-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aece4-400">Az.DataFactory</span></span>
* <span data-ttu-id="aece4-401">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aece4-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="aece4-403">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="aece4-404">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="aece4-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="aece4-405">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aece4-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aece4-406">Az.IotHub</span></span>
* <span data-ttu-id="aece4-407">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aece4-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aece4-408">Az.KeyVault</span></span>
* <span data-ttu-id="aece4-409">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-410">Az.Network</span></span>
* <span data-ttu-id="aece4-411">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-412">Az.Resources</span></span>
* <span data-ttu-id="aece4-413">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="aece4-414">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="aece4-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="aece4-415">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="aece4-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="aece4-416">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="aece4-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="aece4-417">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="aece4-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="aece4-418">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="aece4-419">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="aece4-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aece4-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aece4-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="aece4-421">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="aece4-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="aece4-422">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-422">Fix some error messages.</span></span>
* <span data-ttu-id="aece4-423">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="aece4-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="aece4-424">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="aece4-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aece4-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aece4-425">Az.SignalR</span></span>
* <span data-ttu-id="aece4-426">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-427">Az.Sql</span></span>
* <span data-ttu-id="aece4-428">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aece4-429">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="aece4-430">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="aece4-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="aece4-431">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="aece4-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aece4-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-432">Az.Storage</span></span>
* <span data-ttu-id="aece4-433">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aece4-434">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="aece4-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="aece4-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="aece4-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="aece4-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="aece4-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="aece4-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aece4-437">Az.TrafficManager</span></span>
* <span data-ttu-id="aece4-438">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aece4-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-439">Az.Websites</span></span>
* <span data-ttu-id="aece4-440">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aece4-441">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="aece4-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="aece4-442">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="aece4-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="aece4-443">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="aece4-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aece4-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-444">Az.Accounts</span></span>
* <span data-ttu-id="aece4-445">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-446">Az.Compute</span></span>
* <span data-ttu-id="aece4-447">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="aece4-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="aece4-448">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="aece4-449">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aece4-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="aece4-451">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="aece4-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="aece4-452">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aece4-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aece4-453">Az.EventGrid</span></span>
* <span data-ttu-id="aece4-454">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="aece4-455">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="aece4-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="aece4-456">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="aece4-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aece4-457">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="aece4-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aece4-458">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="aece4-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aece4-459">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="aece4-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="aece4-460">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="aece4-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aece4-461">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="aece4-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aece4-462">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="aece4-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aece4-463">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="aece4-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="aece4-464">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="aece4-465">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="aece4-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aece4-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aece4-466">Az.IotHub</span></span>
* <span data-ttu-id="aece4-467">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aece4-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aece4-468">Az.LogicApp</span></span>
* <span data-ttu-id="aece4-469">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="aece4-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-470">Az.Resources</span></span>
* <span data-ttu-id="aece4-471">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="aece4-472">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="aece4-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="aece4-473">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aece4-474">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="aece4-475">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="aece4-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="aece4-476">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="aece4-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aece4-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aece4-477">Az.SignalR</span></span>
* <span data-ttu-id="aece4-478">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-479">Az.Sql</span></span>
* <span data-ttu-id="aece4-480">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="aece4-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aece4-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-481">Az.Storage</span></span>
* <span data-ttu-id="aece4-482">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="aece4-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="aece4-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aece4-483">New-AzStorageContext</span></span>
* <span data-ttu-id="aece4-484">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="aece4-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="aece4-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="aece4-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aece4-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-486">Az.Websites</span></span>
* <span data-ttu-id="aece4-487">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="aece4-488">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="aece4-489">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="aece4-490">Allgemein</span><span class="sxs-lookup"><span data-stu-id="aece4-490">General</span></span>

- <span data-ttu-id="aece4-491">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="aece4-491">General Availability of Az Module</span></span>
- <span data-ttu-id="aece4-492">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="aece4-492">Online help for each module</span></span>
- <span data-ttu-id="aece4-493">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="aece4-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="aece4-494">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="aece4-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aece4-495">Az.Accounts</span></span>
- <span data-ttu-id="aece4-496">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aece4-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="aece4-497">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="aece4-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aece4-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aece4-498">Az.ApiManagement</span></span>
- <span data-ttu-id="aece4-499">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="aece4-499">Fixes for #7002</span></span>
- <span data-ttu-id="aece4-500">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="aece4-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aece4-501">Az.Batch</span></span>
- <span data-ttu-id="aece4-502">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="aece4-503">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="aece4-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="aece4-504">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="aece4-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="aece4-505">Az.Billing</span></span>
- <span data-ttu-id="aece4-506">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="aece4-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="aece4-507">Az.CognitivServices</span></span>
- <span data-ttu-id="aece4-508">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="aece4-509">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="aece4-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aece4-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="aece4-511">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="aece4-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="aece4-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="aece4-513">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aece4-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="aece4-515">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="aece4-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aece4-516">Az.Monitor</span></span>
- <span data-ttu-id="aece4-517">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="aece4-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aece4-518">Az.KeyVault</span></span>
- <span data-ttu-id="aece4-519">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="aece4-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="aece4-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aece4-520">Az.MachineLearning</span></span>
- <span data-ttu-id="aece4-521">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="aece4-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="aece4-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aece4-522">Az.Media</span></span>
- <span data-ttu-id="aece4-523">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="aece4-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aece4-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-524">Az.Network</span></span>
<span data-ttu-id="aece4-525">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="aece4-526">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="aece4-526">New cmdlets added:</span></span>
        - <span data-ttu-id="aece4-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aece4-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aece4-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aece4-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aece4-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aece4-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aece4-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aece4-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aece4-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aece4-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aece4-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="aece4-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="aece4-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="aece4-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="aece4-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="aece4-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="aece4-535">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="aece4-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aece4-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="aece4-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aece4-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aece4-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aece4-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aece4-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aece4-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="aece4-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="aece4-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="aece4-541">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="aece4-542">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aece4-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="aece4-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aece4-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aece4-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aece4-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aece4-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aece4-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="aece4-546">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="aece4-547">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="aece4-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aece4-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="aece4-549">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="aece4-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aece4-550">Az.Profile</span></span>
- <span data-ttu-id="aece4-551">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="aece4-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="aece4-553">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="aece4-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-554">Az.Resources</span></span>
- <span data-ttu-id="aece4-555">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aece4-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aece4-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="aece4-557">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="aece4-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="aece4-558">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="aece4-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aece4-559">Az.SIgnalR</span></span>
- <span data-ttu-id="aece4-560">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aece4-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="aece4-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-561">Az.Sql</span></span>
- <span data-ttu-id="aece4-562">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="aece4-563">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="aece4-564">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="aece4-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-565">Az.Storage</span></span>
- <span data-ttu-id="aece4-566">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aece4-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-567">Az.Websites</span></span>
- <span data-ttu-id="aece4-568">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aece4-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="aece4-569">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="aece4-570">Allgemein</span><span class="sxs-lookup"><span data-stu-id="aece4-570">General</span></span>

* <span data-ttu-id="aece4-571">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="aece4-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="aece4-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-572">Az.Compute</span></span>

* <span data-ttu-id="aece4-573">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aece4-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="aece4-575">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="aece4-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aece4-576">Az.FrontDoor</span></span>

* <span data-ttu-id="aece4-577">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-577">Fixed some broken links</span></span>
    - <span data-ttu-id="aece4-578">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="aece4-579">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aece4-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aece4-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="aece4-581">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="aece4-582">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="aece4-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="aece4-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-583">Az.Resources</span></span>

* <span data-ttu-id="aece4-584">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="aece4-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="aece4-585">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aece4-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="aece4-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-586">Az.Sql</span></span>

* <span data-ttu-id="aece4-587">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="aece4-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="aece4-588">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="aece4-589">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="aece4-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="aece4-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-590">Az.Storage</span></span>

* <span data-ttu-id="aece4-591">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="aece4-592">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="aece4-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="aece4-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aece4-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aece4-594">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="aece4-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aece4-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="aece4-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aece4-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aece4-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-597">Az.Websites</span></span>

* <span data-ttu-id="aece4-598">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="aece4-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="aece4-599">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aece4-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="aece4-600">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="aece4-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="aece4-601">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aece4-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aece4-602">Az.ApiManagement</span></span>
* <span data-ttu-id="aece4-603">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="aece4-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aece4-604">Az.Automation</span></span>
* <span data-ttu-id="aece4-605">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="aece4-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="aece4-606">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="aece4-607">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="aece4-608">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="aece4-609">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="aece4-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-610">Az.Compute</span></span>
* <span data-ttu-id="aece4-611">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="aece4-612">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aece4-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="aece4-614">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="aece4-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="aece4-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="aece4-616">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aece4-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-617">Az.Network</span></span>
* <span data-ttu-id="aece4-618">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="aece4-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="aece4-619">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="aece4-620">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="aece4-621">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="aece4-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aece4-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aece4-623">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="aece4-624">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="aece4-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="aece4-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aece4-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="aece4-626">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="aece4-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="aece4-627">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="aece4-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="aece4-628">Az.Relay</span></span>
* <span data-ttu-id="aece4-629">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="aece4-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="aece4-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-630">Az.Resources</span></span>
* <span data-ttu-id="aece4-631">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="aece4-632">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="aece4-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="aece4-633">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="aece4-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aece4-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aece4-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="aece4-635">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="aece4-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-636">Az.Sql</span></span>
* <span data-ttu-id="aece4-637">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="aece4-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aece4-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aece4-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aece4-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aece4-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aece4-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aece4-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aece4-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aece4-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aece4-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aece4-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aece4-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aece4-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="aece4-646">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="aece4-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="aece4-647">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="aece4-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="aece4-648">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="aece4-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="aece4-649">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="aece4-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aece4-650">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="aece4-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aece4-651">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="aece4-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="aece4-652">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="aece4-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="aece4-653">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="aece4-654">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aece4-655">Allgemein</span><span class="sxs-lookup"><span data-stu-id="aece4-655">General</span></span>
* <span data-ttu-id="aece4-656">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="aece4-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="aece4-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aece4-657">Az.Profile</span></span>
* <span data-ttu-id="aece4-658">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="aece4-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="aece4-659">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="aece4-660">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="aece4-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="aece4-661">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="aece4-662">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="aece4-663">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="aece4-664">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="aece4-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="aece4-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aece4-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="aece4-666">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-667">Az.Compute</span></span>
* <span data-ttu-id="aece4-668">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="aece4-669">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="aece4-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="aece4-670">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="aece4-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aece4-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="aece4-672">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="aece4-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="aece4-673">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="aece4-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="aece4-674">Az.Insights</span></span>
* <span data-ttu-id="aece4-675">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="aece4-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="aece4-676">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="aece4-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="aece4-677">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="aece4-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="aece4-678">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-679">Az.Network</span></span>
* <span data-ttu-id="aece4-680">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="aece4-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="aece4-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="aece4-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="aece4-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="aece4-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="aece4-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aece4-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="aece4-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="aece4-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="aece4-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="aece4-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="aece4-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aece4-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aece4-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aece4-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="aece4-688">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-689">Az.Resources</span></span>
* <span data-ttu-id="aece4-690">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="aece4-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="aece4-691">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="aece4-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aece4-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aece4-692">Az.ServiceBus</span></span>
* <span data-ttu-id="aece4-693">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="aece4-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aece4-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aece4-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="aece4-695">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="aece4-696">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="aece4-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="aece4-697">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="aece4-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="aece4-698">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="aece4-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="aece4-699">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="aece4-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="aece4-700">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="aece4-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aece4-701">Az.Profile</span></span>
* <span data-ttu-id="aece4-702">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="aece4-703">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="aece4-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-704">Az.Compute</span></span>
* <span data-ttu-id="aece4-705">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="aece4-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="aece4-706">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aece4-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aece4-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="aece4-708">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="aece4-709">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="aece4-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="aece4-710">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="aece4-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aece4-711">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="aece4-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aece4-712">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="aece4-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-713">Az.Network</span></span>
* <span data-ttu-id="aece4-714">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="aece4-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="aece4-715">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-716">Az.Resources</span></span>
* <span data-ttu-id="aece4-717">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="aece4-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="aece4-718">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aece4-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="aece4-719">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="aece4-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="aece4-720">Azure.Storage</span></span>
* <span data-ttu-id="aece4-721">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="aece4-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="aece4-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="aece4-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="aece4-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aece4-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aece4-724">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="aece4-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="aece4-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="aece4-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="aece4-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aece4-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="aece4-727">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aece4-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aece4-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aece4-728">Az.Compute</span></span>
* <span data-ttu-id="aece4-729">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="aece4-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="aece4-730">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="aece4-731">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="aece4-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="aece4-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aece4-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="aece4-733">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aece4-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aece4-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aece4-734">Az.Network</span></span>
* <span data-ttu-id="aece4-735">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aece4-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="aece4-736">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-736">new cmdlets added</span></span>
    - <span data-ttu-id="aece4-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aece4-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="aece4-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aece4-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="aece4-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aece4-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="aece4-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aece4-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="aece4-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="aece4-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="aece4-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="aece4-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="aece4-743">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="aece4-744">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="aece4-745">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aece4-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aece4-746">Az.RedisCache</span></span>
* <span data-ttu-id="aece4-747">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="aece4-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="aece4-748">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="aece4-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aece4-749">Az.Resources</span></span>
* <span data-ttu-id="aece4-750">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="aece4-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aece4-751">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="aece4-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="aece4-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aece4-752">Az.Sql</span></span>
* <span data-ttu-id="aece4-753">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="aece4-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aece4-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aece4-754">Az.Websites</span></span>
* <span data-ttu-id="aece4-755">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="aece4-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="aece4-756">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="aece4-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="aece4-757">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="aece4-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="aece4-758">Erste Version</span><span class="sxs-lookup"><span data-stu-id="aece4-758">Initial Release</span></span>