---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1cc7d6519ded41003daed558a8e78ee65ded072a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240963"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="054bf-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="054bf-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="054bf-104">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="054bf-105">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="054bf-105">Highlights since the last major release</span></span>
* <span data-ttu-id="054bf-106">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="054bf-106">General availability of `Az` module</span></span>
* <span data-ttu-id="054bf-107">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="054bf-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="054bf-108">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="054bf-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="054bf-109">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="054bf-110">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="054bf-111">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="054bf-112">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="054bf-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-113">Az.Accounts</span></span>
* <span data-ttu-id="054bf-114">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="054bf-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="054bf-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="054bf-115">Az.Batch</span></span>
* <span data-ttu-id="054bf-116">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="054bf-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="054bf-117">Az.Cdn</span></span>
* <span data-ttu-id="054bf-118">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="054bf-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="054bf-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="054bf-120">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-121">Az.Compute</span></span>
* <span data-ttu-id="054bf-122">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="054bf-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="054bf-123">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="054bf-124">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="054bf-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="054bf-125">Az.DataFactory</span></span>
* <span data-ttu-id="054bf-126">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="054bf-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="054bf-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="054bf-128">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="054bf-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="054bf-129">Az.EventGrid</span></span>
* <span data-ttu-id="054bf-130">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="054bf-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="054bf-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="054bf-131">Az.EventHub</span></span>
* <span data-ttu-id="054bf-132">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="054bf-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="054bf-133">Az.HDInsight</span></span>
* <span data-ttu-id="054bf-134">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="054bf-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="054bf-135">Az.IotHub</span></span>
* <span data-ttu-id="054bf-136">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="054bf-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="054bf-137">Az.KeyVault</span></span>
* <span data-ttu-id="054bf-138">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="054bf-139">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="054bf-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="054bf-140">Az.MachineLearning</span></span>
* <span data-ttu-id="054bf-141">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="054bf-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="054bf-142">Az.Media</span></span>
* <span data-ttu-id="054bf-143">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="054bf-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="054bf-144">Az.Monitor</span></span>
  * <span data-ttu-id="054bf-145">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="054bf-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="054bf-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="054bf-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="054bf-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="054bf-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="054bf-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="054bf-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="054bf-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="054bf-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="054bf-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="054bf-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="054bf-151">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-152">Az.Network</span></span>
* <span data-ttu-id="054bf-153">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="054bf-154">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="054bf-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="054bf-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="054bf-156">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="054bf-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="054bf-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="054bf-158">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="054bf-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="054bf-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="054bf-160">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="054bf-162">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="054bf-163">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="054bf-164">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="054bf-165">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="054bf-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="054bf-166">Az.RedisCache</span></span>
* <span data-ttu-id="054bf-167">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-168">Az.Resources</span></span>
* <span data-ttu-id="054bf-169">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-170">Az.Sql</span></span>
* <span data-ttu-id="054bf-171">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="054bf-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="054bf-172">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="054bf-173">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="054bf-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="054bf-174">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="054bf-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="054bf-175">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="054bf-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="054bf-176">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="054bf-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="054bf-177">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="054bf-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-178">Az.Websites</span></span>
* <span data-ttu-id="054bf-179">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="054bf-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="054bf-180">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="054bf-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="054bf-181">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="054bf-182">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="054bf-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="054bf-183">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="054bf-184">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="054bf-184">Highlights since the last major release</span></span>
* <span data-ttu-id="054bf-185">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="054bf-185">General availability of `Az` module</span></span>
* <span data-ttu-id="054bf-186">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="054bf-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="054bf-187">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="054bf-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="054bf-188">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="054bf-189">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="054bf-190">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="054bf-191">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="054bf-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-192">Az.Accounts</span></span>
* <span data-ttu-id="054bf-193">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="054bf-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="054bf-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="054bf-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="054bf-195">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="054bf-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="054bf-196">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="054bf-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="054bf-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="054bf-197">Az.Automation</span></span>
* <span data-ttu-id="054bf-198">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="054bf-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="054bf-199">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="054bf-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="054bf-200">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="054bf-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-201">Az.Compute</span></span>
* <span data-ttu-id="054bf-202">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="054bf-203">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="054bf-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="054bf-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="054bf-205">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="054bf-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="054bf-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="054bf-206">Az.DataFactory</span></span>
* <span data-ttu-id="054bf-207">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="054bf-208">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-209">Az.Resources</span></span>
* <span data-ttu-id="054bf-210">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="054bf-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="054bf-211">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="054bf-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="054bf-212">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="054bf-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="054bf-213">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="054bf-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="054bf-214">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="054bf-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="054bf-215">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="054bf-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-216">Az.Sql</span></span>
* <span data-ttu-id="054bf-217">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="054bf-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="054bf-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-218">Az.Storage</span></span>
* <span data-ttu-id="054bf-219">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="054bf-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="054bf-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="054bf-220">New-AzStorageContext</span></span>
* <span data-ttu-id="054bf-221">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="054bf-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="054bf-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="054bf-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="054bf-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="054bf-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="054bf-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="054bf-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="054bf-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="054bf-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="054bf-226">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="054bf-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="054bf-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="054bf-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="054bf-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="054bf-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="054bf-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="054bf-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="054bf-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="054bf-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="054bf-231">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="054bf-232">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="054bf-232">Highlights since the last major release</span></span>
* <span data-ttu-id="054bf-233">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="054bf-233">General availability of `Az` module</span></span>
* <span data-ttu-id="054bf-234">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="054bf-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="054bf-235">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="054bf-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="054bf-236">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="054bf-237">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="054bf-238">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="054bf-239">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="054bf-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="054bf-240">Az.Automation</span></span>
* <span data-ttu-id="054bf-241">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="054bf-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="054bf-242">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="054bf-242">Dynamic grouping</span></span>
    * <span data-ttu-id="054bf-243">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="054bf-243">Pre-Post script</span></span>
    * <span data-ttu-id="054bf-244">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="054bf-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-245">Az.Compute</span></span>
* <span data-ttu-id="054bf-246">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="054bf-247">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="054bf-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="054bf-248">Az.KeyVault</span></span>
* <span data-ttu-id="054bf-249">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-250">Az.Network</span></span>
* <span data-ttu-id="054bf-251">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="054bf-252">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="054bf-254">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="054bf-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="054bf-255">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-256">Az.Resources</span></span>
* <span data-ttu-id="054bf-257">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="054bf-258">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="054bf-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-259">Az.Sql</span></span>
* <span data-ttu-id="054bf-260">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="054bf-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="054bf-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-261">Az.Storage</span></span>
* <span data-ttu-id="054bf-262">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="054bf-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="054bf-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="054bf-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="054bf-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="054bf-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="054bf-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="054bf-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="054bf-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="054bf-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="054bf-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="054bf-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="054bf-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="054bf-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-269">Az.Websites</span></span>
* <span data-ttu-id="054bf-270">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="054bf-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="054bf-271">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="054bf-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-272">Az.Accounts</span></span>
* <span data-ttu-id="054bf-273">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="054bf-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="054bf-274">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="054bf-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="054bf-275">Az.Automation</span></span>
* <span data-ttu-id="054bf-276">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="054bf-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="054bf-277">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="054bf-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="054bf-278">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="054bf-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="054bf-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="054bf-279">Az.Cdn</span></span>
* <span data-ttu-id="054bf-280">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="054bf-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-281">Az.Compute</span></span>
* <span data-ttu-id="054bf-282">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="054bf-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="054bf-283">Az.DataFactory</span></span>
* <span data-ttu-id="054bf-284">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="054bf-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="054bf-285">Az.LogicApp</span></span>
* <span data-ttu-id="054bf-286">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="054bf-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-287">Az.Network</span></span>
* <span data-ttu-id="054bf-288">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="054bf-290">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="054bf-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="054bf-291">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="054bf-291">SDK Update</span></span>
* <span data-ttu-id="054bf-292">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="054bf-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="054bf-293">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-294">Az.Resources</span></span>
* <span data-ttu-id="054bf-295">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="054bf-296">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="054bf-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="054bf-297">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="054bf-298">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="054bf-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="054bf-299">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="054bf-300">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="054bf-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-301">Az.Sql</span></span>
* <span data-ttu-id="054bf-302">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="054bf-303">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="054bf-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-304">Az.Storage</span></span>
* <span data-ttu-id="054bf-305">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="054bf-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="054bf-306">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="054bf-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="054bf-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="054bf-308">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="054bf-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="054bf-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="054bf-309">Az.Automation</span></span>
* <span data-ttu-id="054bf-310">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="054bf-311">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="054bf-312">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="054bf-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="054bf-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="054bf-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="054bf-314">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="054bf-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-315">Az.Compute</span></span>
* <span data-ttu-id="054bf-316">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="054bf-317">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="054bf-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="054bf-318">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="054bf-319">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="054bf-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="054bf-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="054bf-321">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="054bf-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="054bf-322">Az.EventHub</span></span>
* <span data-ttu-id="054bf-323">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="054bf-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="054bf-324">Az.KeyVault</span></span>
* <span data-ttu-id="054bf-325">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="054bf-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="054bf-326">Az.LogicApp</span></span>
* <span data-ttu-id="054bf-327">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="054bf-328">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="054bf-329">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="054bf-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="054bf-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="054bf-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="054bf-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="054bf-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="054bf-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="054bf-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="054bf-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="054bf-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="054bf-334">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="054bf-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="054bf-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="054bf-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="054bf-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="054bf-339">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="054bf-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="054bf-340">Az.Monitor</span></span>
* <span data-ttu-id="054bf-341">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-342">Az.Network</span></span>
* <span data-ttu-id="054bf-343">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="054bf-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="054bf-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="054bf-345">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="054bf-346">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="054bf-347">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="054bf-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-348">Az.Resources</span></span>
* <span data-ttu-id="054bf-349">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="054bf-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="054bf-350">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="054bf-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="054bf-351">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="054bf-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="054bf-352">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="054bf-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-353">Az.Sql</span></span>
* <span data-ttu-id="054bf-354">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="054bf-355">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="054bf-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="054bf-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-356">Az.Websites</span></span>
* <span data-ttu-id="054bf-357">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="054bf-358">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="054bf-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-359">Az.Accounts</span></span>
* <span data-ttu-id="054bf-360">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="054bf-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="054bf-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="054bf-361">Az.AnalysisServices</span></span>
<span data-ttu-id="054bf-362">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="054bf-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-363">Az.Compute</span></span>
* <span data-ttu-id="054bf-364">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="054bf-365">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="054bf-366">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-367">Az.RecoveryServices</span></span>
<span data-ttu-id="054bf-368">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="054bf-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-369">Az.Resources</span></span>
* <span data-ttu-id="054bf-370">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="054bf-371">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="054bf-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="054bf-372">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="054bf-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="054bf-373">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="054bf-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-374">Az.Sql</span></span>
* <span data-ttu-id="054bf-375">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="054bf-376">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="054bf-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="054bf-377">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="054bf-378">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="054bf-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-379">Az.Accounts</span></span>
* <span data-ttu-id="054bf-380">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="054bf-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="054bf-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="054bf-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="054bf-382">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="054bf-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="054bf-384">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="054bf-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="054bf-385">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="054bf-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-386">Az.Accounts</span></span>
* <span data-ttu-id="054bf-387">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="054bf-388">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="054bf-389">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="054bf-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="054bf-390">Az.Aks</span></span>
* <span data-ttu-id="054bf-391">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="054bf-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="054bf-392">Az.Automation</span></span>
* <span data-ttu-id="054bf-393">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="054bf-394">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="054bf-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="054bf-395">Az.Cdn</span></span>
* <span data-ttu-id="054bf-396">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-397">Az.Compute</span></span>
* <span data-ttu-id="054bf-398">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="054bf-399">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="054bf-400">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="054bf-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="054bf-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="054bf-402">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="054bf-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="054bf-403">Az.DataFactory</span></span>
* <span data-ttu-id="054bf-404">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="054bf-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="054bf-406">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="054bf-407">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="054bf-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="054bf-408">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="054bf-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="054bf-409">Az.IotHub</span></span>
* <span data-ttu-id="054bf-410">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="054bf-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="054bf-411">Az.KeyVault</span></span>
* <span data-ttu-id="054bf-412">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-413">Az.Network</span></span>
* <span data-ttu-id="054bf-414">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-415">Az.Resources</span></span>
* <span data-ttu-id="054bf-416">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="054bf-417">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="054bf-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="054bf-418">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="054bf-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="054bf-419">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="054bf-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="054bf-420">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="054bf-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="054bf-421">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="054bf-422">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="054bf-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="054bf-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="054bf-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="054bf-424">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="054bf-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="054bf-425">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-425">Fix some error messages.</span></span>
* <span data-ttu-id="054bf-426">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="054bf-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="054bf-427">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="054bf-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="054bf-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="054bf-428">Az.SignalR</span></span>
* <span data-ttu-id="054bf-429">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-430">Az.Sql</span></span>
* <span data-ttu-id="054bf-431">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="054bf-432">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="054bf-433">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="054bf-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="054bf-434">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="054bf-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="054bf-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-435">Az.Storage</span></span>
* <span data-ttu-id="054bf-436">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="054bf-437">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="054bf-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="054bf-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="054bf-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="054bf-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="054bf-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="054bf-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="054bf-440">Az.TrafficManager</span></span>
* <span data-ttu-id="054bf-441">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="054bf-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-442">Az.Websites</span></span>
* <span data-ttu-id="054bf-443">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="054bf-444">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="054bf-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="054bf-445">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="054bf-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="054bf-446">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="054bf-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="054bf-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-447">Az.Accounts</span></span>
* <span data-ttu-id="054bf-448">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-449">Az.Compute</span></span>
* <span data-ttu-id="054bf-450">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="054bf-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="054bf-451">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="054bf-452">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="054bf-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="054bf-454">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="054bf-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="054bf-455">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="054bf-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="054bf-456">Az.EventGrid</span></span>
* <span data-ttu-id="054bf-457">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="054bf-458">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="054bf-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="054bf-459">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="054bf-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="054bf-460">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="054bf-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="054bf-461">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="054bf-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="054bf-462">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="054bf-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="054bf-463">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="054bf-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="054bf-464">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="054bf-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="054bf-465">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="054bf-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="054bf-466">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="054bf-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="054bf-467">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="054bf-468">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="054bf-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="054bf-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="054bf-469">Az.IotHub</span></span>
* <span data-ttu-id="054bf-470">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="054bf-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="054bf-471">Az.LogicApp</span></span>
* <span data-ttu-id="054bf-472">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="054bf-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-473">Az.Resources</span></span>
* <span data-ttu-id="054bf-474">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="054bf-475">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="054bf-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="054bf-476">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="054bf-477">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="054bf-478">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="054bf-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="054bf-479">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="054bf-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="054bf-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="054bf-480">Az.SignalR</span></span>
* <span data-ttu-id="054bf-481">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-482">Az.Sql</span></span>
* <span data-ttu-id="054bf-483">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="054bf-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="054bf-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-484">Az.Storage</span></span>
* <span data-ttu-id="054bf-485">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="054bf-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="054bf-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="054bf-486">New-AzStorageContext</span></span>
* <span data-ttu-id="054bf-487">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="054bf-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="054bf-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="054bf-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="054bf-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-489">Az.Websites</span></span>
* <span data-ttu-id="054bf-490">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="054bf-491">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="054bf-492">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="054bf-493">Allgemein</span><span class="sxs-lookup"><span data-stu-id="054bf-493">General</span></span>

- <span data-ttu-id="054bf-494">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="054bf-494">General Availability of Az Module</span></span>
- <span data-ttu-id="054bf-495">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="054bf-495">Online help for each module</span></span>
- <span data-ttu-id="054bf-496">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="054bf-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="054bf-497">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="054bf-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="054bf-498">Az.Accounts</span></span>
- <span data-ttu-id="054bf-499">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="054bf-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="054bf-500">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="054bf-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="054bf-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="054bf-501">Az.ApiManagement</span></span>
- <span data-ttu-id="054bf-502">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="054bf-502">Fixes for #7002</span></span>
- <span data-ttu-id="054bf-503">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="054bf-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="054bf-504">Az.Batch</span></span>
- <span data-ttu-id="054bf-505">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="054bf-506">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="054bf-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="054bf-507">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="054bf-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="054bf-508">Az.Billing</span></span>
- <span data-ttu-id="054bf-509">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="054bf-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="054bf-510">Az.CognitivServices</span></span>
- <span data-ttu-id="054bf-511">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="054bf-512">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="054bf-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="054bf-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="054bf-514">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="054bf-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="054bf-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="054bf-516">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="054bf-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="054bf-518">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="054bf-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="054bf-519">Az.Monitor</span></span>
- <span data-ttu-id="054bf-520">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="054bf-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="054bf-521">Az.KeyVault</span></span>
- <span data-ttu-id="054bf-522">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="054bf-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="054bf-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="054bf-523">Az.MachineLearning</span></span>
- <span data-ttu-id="054bf-524">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="054bf-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="054bf-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="054bf-525">Az.Media</span></span>
- <span data-ttu-id="054bf-526">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="054bf-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="054bf-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-527">Az.Network</span></span>
<span data-ttu-id="054bf-528">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="054bf-529">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="054bf-529">New cmdlets added:</span></span>
        - <span data-ttu-id="054bf-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054bf-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="054bf-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054bf-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="054bf-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054bf-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="054bf-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054bf-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="054bf-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054bf-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="054bf-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="054bf-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="054bf-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="054bf-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="054bf-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="054bf-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="054bf-538">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="054bf-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="054bf-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="054bf-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="054bf-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="054bf-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="054bf-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="054bf-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="054bf-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="054bf-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="054bf-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="054bf-544">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="054bf-545">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="054bf-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="054bf-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="054bf-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="054bf-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="054bf-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="054bf-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="054bf-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="054bf-549">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="054bf-550">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="054bf-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="054bf-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="054bf-552">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="054bf-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="054bf-553">Az.Profile</span></span>
- <span data-ttu-id="054bf-554">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="054bf-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="054bf-556">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="054bf-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-557">Az.Resources</span></span>
- <span data-ttu-id="054bf-558">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="054bf-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="054bf-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="054bf-560">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="054bf-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="054bf-561">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="054bf-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="054bf-562">Az.SIgnalR</span></span>
- <span data-ttu-id="054bf-563">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="054bf-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="054bf-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-564">Az.Sql</span></span>
- <span data-ttu-id="054bf-565">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="054bf-566">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="054bf-567">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="054bf-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-568">Az.Storage</span></span>
- <span data-ttu-id="054bf-569">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="054bf-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-570">Az.Websites</span></span>
- <span data-ttu-id="054bf-571">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="054bf-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="054bf-572">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="054bf-573">Allgemein</span><span class="sxs-lookup"><span data-stu-id="054bf-573">General</span></span>

* <span data-ttu-id="054bf-574">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="054bf-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="054bf-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-575">Az.Compute</span></span>

* <span data-ttu-id="054bf-576">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="054bf-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="054bf-578">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="054bf-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="054bf-579">Az.FrontDoor</span></span>

* <span data-ttu-id="054bf-580">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-580">Fixed some broken links</span></span>
    - <span data-ttu-id="054bf-581">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="054bf-582">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="054bf-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="054bf-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="054bf-584">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="054bf-585">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="054bf-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="054bf-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-586">Az.Resources</span></span>

* <span data-ttu-id="054bf-587">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="054bf-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="054bf-588">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="054bf-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="054bf-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-589">Az.Sql</span></span>

* <span data-ttu-id="054bf-590">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="054bf-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="054bf-591">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="054bf-592">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="054bf-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="054bf-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-593">Az.Storage</span></span>

* <span data-ttu-id="054bf-594">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="054bf-595">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="054bf-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="054bf-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="054bf-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="054bf-597">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="054bf-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="054bf-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="054bf-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="054bf-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="054bf-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-600">Az.Websites</span></span>

* <span data-ttu-id="054bf-601">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="054bf-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="054bf-602">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="054bf-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="054bf-603">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="054bf-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="054bf-604">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="054bf-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="054bf-605">Az.ApiManagement</span></span>
* <span data-ttu-id="054bf-606">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="054bf-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="054bf-607">Az.Automation</span></span>
* <span data-ttu-id="054bf-608">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="054bf-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="054bf-609">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="054bf-610">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="054bf-611">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="054bf-612">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="054bf-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-613">Az.Compute</span></span>
* <span data-ttu-id="054bf-614">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="054bf-615">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="054bf-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="054bf-617">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="054bf-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="054bf-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="054bf-619">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="054bf-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-620">Az.Network</span></span>
* <span data-ttu-id="054bf-621">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="054bf-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="054bf-622">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="054bf-623">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="054bf-624">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="054bf-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="054bf-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="054bf-626">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="054bf-627">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="054bf-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="054bf-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="054bf-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="054bf-629">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="054bf-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="054bf-630">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="054bf-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="054bf-631">Az.Relay</span></span>
* <span data-ttu-id="054bf-632">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="054bf-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="054bf-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-633">Az.Resources</span></span>
* <span data-ttu-id="054bf-634">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="054bf-635">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="054bf-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="054bf-636">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="054bf-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="054bf-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="054bf-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="054bf-638">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="054bf-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-639">Az.Sql</span></span>
* <span data-ttu-id="054bf-640">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="054bf-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="054bf-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="054bf-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="054bf-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="054bf-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="054bf-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="054bf-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="054bf-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="054bf-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="054bf-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="054bf-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="054bf-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="054bf-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="054bf-649">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="054bf-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="054bf-650">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="054bf-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="054bf-651">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="054bf-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="054bf-652">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="054bf-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="054bf-653">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="054bf-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="054bf-654">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="054bf-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="054bf-655">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="054bf-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="054bf-656">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="054bf-657">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="054bf-658">Allgemein</span><span class="sxs-lookup"><span data-stu-id="054bf-658">General</span></span>
* <span data-ttu-id="054bf-659">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="054bf-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="054bf-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="054bf-660">Az.Profile</span></span>
* <span data-ttu-id="054bf-661">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="054bf-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="054bf-662">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="054bf-663">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="054bf-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="054bf-664">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="054bf-665">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="054bf-666">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="054bf-667">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="054bf-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="054bf-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="054bf-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="054bf-669">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-670">Az.Compute</span></span>
* <span data-ttu-id="054bf-671">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="054bf-672">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="054bf-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="054bf-673">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="054bf-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="054bf-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="054bf-675">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="054bf-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="054bf-676">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="054bf-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="054bf-677">Az.Insights</span></span>
* <span data-ttu-id="054bf-678">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="054bf-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="054bf-679">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="054bf-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="054bf-680">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="054bf-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="054bf-681">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-682">Az.Network</span></span>
* <span data-ttu-id="054bf-683">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="054bf-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="054bf-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="054bf-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="054bf-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="054bf-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="054bf-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="054bf-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="054bf-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="054bf-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="054bf-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="054bf-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="054bf-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="054bf-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="054bf-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="054bf-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="054bf-691">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-692">Az.Resources</span></span>
* <span data-ttu-id="054bf-693">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="054bf-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="054bf-694">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="054bf-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="054bf-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="054bf-695">Az.ServiceBus</span></span>
* <span data-ttu-id="054bf-696">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="054bf-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="054bf-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="054bf-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="054bf-698">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="054bf-699">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="054bf-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="054bf-700">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="054bf-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="054bf-701">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="054bf-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="054bf-702">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="054bf-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="054bf-703">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="054bf-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="054bf-704">Az.Profile</span></span>
* <span data-ttu-id="054bf-705">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="054bf-706">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="054bf-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-707">Az.Compute</span></span>
* <span data-ttu-id="054bf-708">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="054bf-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="054bf-709">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="054bf-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="054bf-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="054bf-711">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="054bf-712">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="054bf-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="054bf-713">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="054bf-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="054bf-714">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="054bf-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="054bf-715">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="054bf-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-716">Az.Network</span></span>
* <span data-ttu-id="054bf-717">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="054bf-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="054bf-718">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-719">Az.Resources</span></span>
* <span data-ttu-id="054bf-720">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="054bf-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="054bf-721">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="054bf-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="054bf-722">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="054bf-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="054bf-723">Azure.Storage</span></span>
* <span data-ttu-id="054bf-724">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="054bf-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="054bf-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="054bf-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="054bf-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="054bf-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="054bf-727">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="054bf-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="054bf-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="054bf-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="054bf-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="054bf-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="054bf-730">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="054bf-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="054bf-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="054bf-731">Az.Compute</span></span>
* <span data-ttu-id="054bf-732">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="054bf-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="054bf-733">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="054bf-734">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="054bf-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="054bf-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="054bf-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="054bf-736">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="054bf-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="054bf-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="054bf-737">Az.Network</span></span>
* <span data-ttu-id="054bf-738">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="054bf-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="054bf-739">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-739">new cmdlets added</span></span>
    - <span data-ttu-id="054bf-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="054bf-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="054bf-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="054bf-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="054bf-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="054bf-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="054bf-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="054bf-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="054bf-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="054bf-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="054bf-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="054bf-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="054bf-746">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="054bf-747">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="054bf-748">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="054bf-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="054bf-749">Az.RedisCache</span></span>
* <span data-ttu-id="054bf-750">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="054bf-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="054bf-751">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="054bf-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="054bf-752">Az.Resources</span></span>
* <span data-ttu-id="054bf-753">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="054bf-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="054bf-754">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="054bf-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="054bf-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="054bf-755">Az.Sql</span></span>
* <span data-ttu-id="054bf-756">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="054bf-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="054bf-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="054bf-757">Az.Websites</span></span>
* <span data-ttu-id="054bf-758">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="054bf-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="054bf-759">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="054bf-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="054bf-760">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="054bf-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="054bf-761">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="054bf-761">Initial Release</span></span>
