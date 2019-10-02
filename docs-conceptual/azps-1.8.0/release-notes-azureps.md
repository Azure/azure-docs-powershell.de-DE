---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319306"
---
## <a name="180---april-2019"></a><span data-ttu-id="0eaac-103">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eaac-104">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0eaac-104">Highlights since the last major release</span></span>
* <span data-ttu-id="0eaac-105">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="0eaac-105">General availability of `Az` module</span></span>
* <span data-ttu-id="0eaac-106">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="0eaac-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0eaac-107">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="0eaac-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0eaac-108">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0eaac-109">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eaac-110">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0eaac-111">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eaac-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-112">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-113">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="0eaac-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0eaac-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eaac-114">Az.Batch</span></span>
* <span data-ttu-id="0eaac-115">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eaac-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eaac-116">Az.Cdn</span></span>
* <span data-ttu-id="0eaac-117">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eaac-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eaac-119">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-120">Az.Compute</span></span>
* <span data-ttu-id="0eaac-121">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="0eaac-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0eaac-122">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eaac-123">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eaac-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eaac-124">Az.DataFactory</span></span>
* <span data-ttu-id="0eaac-125">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="0eaac-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eaac-127">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0eaac-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0eaac-128">Az.EventGrid</span></span>
* <span data-ttu-id="0eaac-129">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0eaac-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eaac-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eaac-130">Az.EventHub</span></span>
* <span data-ttu-id="0eaac-131">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0eaac-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eaac-132">Az.HDInsight</span></span>
* <span data-ttu-id="0eaac-133">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eaac-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eaac-134">Az.IotHub</span></span>
* <span data-ttu-id="0eaac-135">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eaac-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eaac-136">Az.KeyVault</span></span>
* <span data-ttu-id="0eaac-137">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eaac-138">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0eaac-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0eaac-139">Az.MachineLearning</span></span>
* <span data-ttu-id="0eaac-140">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0eaac-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0eaac-141">Az.Media</span></span>
* <span data-ttu-id="0eaac-142">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eaac-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eaac-143">Az.Monitor</span></span>
  * <span data-ttu-id="0eaac-144">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="0eaac-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0eaac-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0eaac-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0eaac-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0eaac-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0eaac-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0eaac-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0eaac-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0eaac-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0eaac-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0eaac-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0eaac-150">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-151">Az.Network</span></span>
* <span data-ttu-id="0eaac-152">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eaac-153">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0eaac-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0eaac-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="0eaac-155">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eaac-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eaac-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eaac-157">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0eaac-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0eaac-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0eaac-159">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eaac-161">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eaac-162">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0eaac-163">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0eaac-164">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0eaac-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0eaac-165">Az.RedisCache</span></span>
* <span data-ttu-id="0eaac-166">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-167">Az.Resources</span></span>
* <span data-ttu-id="0eaac-168">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-169">Az.Sql</span></span>
* <span data-ttu-id="0eaac-170">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="0eaac-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0eaac-171">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eaac-172">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="0eaac-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0eaac-173">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0eaac-174">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="0eaac-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0eaac-175">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="0eaac-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0eaac-176">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eaac-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-177">Az.Websites</span></span>
* <span data-ttu-id="0eaac-178">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="0eaac-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0eaac-179">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0eaac-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eaac-180">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0eaac-181">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="0eaac-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0eaac-182">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eaac-183">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0eaac-183">Highlights since the last major release</span></span>
* <span data-ttu-id="0eaac-184">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="0eaac-184">General availability of `Az` module</span></span>
* <span data-ttu-id="0eaac-185">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="0eaac-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0eaac-186">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="0eaac-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0eaac-187">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0eaac-188">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eaac-189">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0eaac-190">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eaac-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-191">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-192">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="0eaac-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0eaac-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="0eaac-194">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0eaac-195">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0eaac-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eaac-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eaac-196">Az.Automation</span></span>
* <span data-ttu-id="0eaac-197">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="0eaac-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0eaac-198">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0eaac-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0eaac-199">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="0eaac-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-200">Az.Compute</span></span>
* <span data-ttu-id="0eaac-201">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0eaac-202">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="0eaac-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0eaac-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="0eaac-204">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="0eaac-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eaac-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eaac-205">Az.DataFactory</span></span>
* <span data-ttu-id="0eaac-206">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0eaac-207">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-208">Az.Resources</span></span>
* <span data-ttu-id="0eaac-209">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0eaac-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0eaac-210">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0eaac-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0eaac-211">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="0eaac-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0eaac-212">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0eaac-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0eaac-213">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="0eaac-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0eaac-214">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0eaac-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-215">Az.Sql</span></span>
* <span data-ttu-id="0eaac-216">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="0eaac-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eaac-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-217">Az.Storage</span></span>
* <span data-ttu-id="0eaac-218">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="0eaac-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0eaac-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0eaac-219">New-AzStorageContext</span></span>
* <span data-ttu-id="0eaac-220">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="0eaac-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0eaac-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0eaac-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0eaac-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0eaac-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0eaac-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0eaac-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0eaac-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0eaac-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0eaac-225">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="0eaac-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0eaac-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0eaac-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0eaac-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0eaac-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0eaac-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0eaac-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0eaac-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0eaac-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0eaac-230">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eaac-231">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="0eaac-231">Highlights since the last major release</span></span>
* <span data-ttu-id="0eaac-232">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="0eaac-232">General availability of `Az` module</span></span>
* <span data-ttu-id="0eaac-233">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="0eaac-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0eaac-234">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="0eaac-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0eaac-235">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0eaac-236">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eaac-237">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0eaac-238">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eaac-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eaac-239">Az.Automation</span></span>
* <span data-ttu-id="0eaac-240">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="0eaac-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0eaac-241">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="0eaac-241">Dynamic grouping</span></span>
    * <span data-ttu-id="0eaac-242">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="0eaac-242">Pre-Post script</span></span>
    * <span data-ttu-id="0eaac-243">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="0eaac-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-244">Az.Compute</span></span>
* <span data-ttu-id="0eaac-245">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0eaac-246">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eaac-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eaac-247">Az.KeyVault</span></span>
* <span data-ttu-id="0eaac-248">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-249">Az.Network</span></span>
* <span data-ttu-id="0eaac-250">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0eaac-251">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eaac-253">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0eaac-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0eaac-254">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-255">Az.Resources</span></span>
* <span data-ttu-id="0eaac-256">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0eaac-257">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0eaac-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-258">Az.Sql</span></span>
* <span data-ttu-id="0eaac-259">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0eaac-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eaac-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-260">Az.Storage</span></span>
* <span data-ttu-id="0eaac-261">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0eaac-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0eaac-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0eaac-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0eaac-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0eaac-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0eaac-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0eaac-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0eaac-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0eaac-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0eaac-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0eaac-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0eaac-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eaac-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-268">Az.Websites</span></span>
* <span data-ttu-id="0eaac-269">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="0eaac-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0eaac-270">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eaac-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-271">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-272">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0eaac-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0eaac-273">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eaac-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eaac-274">Az.Automation</span></span>
* <span data-ttu-id="0eaac-275">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="0eaac-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0eaac-276">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="0eaac-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0eaac-277">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0eaac-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eaac-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eaac-278">Az.Cdn</span></span>
* <span data-ttu-id="0eaac-279">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="0eaac-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-280">Az.Compute</span></span>
* <span data-ttu-id="0eaac-281">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eaac-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eaac-282">Az.DataFactory</span></span>
* <span data-ttu-id="0eaac-283">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eaac-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eaac-284">Az.LogicApp</span></span>
* <span data-ttu-id="0eaac-285">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0eaac-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-286">Az.Network</span></span>
* <span data-ttu-id="0eaac-287">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eaac-289">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="0eaac-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0eaac-290">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="0eaac-290">SDK Update</span></span>
* <span data-ttu-id="0eaac-291">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="0eaac-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0eaac-292">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-293">Az.Resources</span></span>
* <span data-ttu-id="0eaac-294">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0eaac-295">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0eaac-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0eaac-296">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0eaac-297">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0eaac-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0eaac-298">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0eaac-299">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0eaac-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-300">Az.Sql</span></span>
* <span data-ttu-id="0eaac-301">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0eaac-302">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eaac-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-303">Az.Storage</span></span>
* <span data-ttu-id="0eaac-304">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eaac-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0eaac-305">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0eaac-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="0eaac-307">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eaac-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eaac-308">Az.Automation</span></span>
* <span data-ttu-id="0eaac-309">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0eaac-310">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0eaac-311">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="0eaac-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eaac-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eaac-313">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0eaac-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-314">Az.Compute</span></span>
* <span data-ttu-id="0eaac-315">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0eaac-316">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="0eaac-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0eaac-317">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0eaac-318">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="0eaac-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eaac-320">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eaac-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eaac-321">Az.EventHub</span></span>
* <span data-ttu-id="0eaac-322">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0eaac-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eaac-323">Az.KeyVault</span></span>
* <span data-ttu-id="0eaac-324">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eaac-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eaac-325">Az.LogicApp</span></span>
* <span data-ttu-id="0eaac-326">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0eaac-327">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0eaac-328">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="0eaac-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0eaac-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eaac-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0eaac-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eaac-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0eaac-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eaac-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0eaac-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eaac-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0eaac-333">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0eaac-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0eaac-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0eaac-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0eaac-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0eaac-338">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eaac-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eaac-339">Az.Monitor</span></span>
* <span data-ttu-id="0eaac-340">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-341">Az.Network</span></span>
* <span data-ttu-id="0eaac-342">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eaac-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eaac-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eaac-344">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0eaac-345">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0eaac-346">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="0eaac-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0eaac-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-347">Az.Resources</span></span>
* <span data-ttu-id="0eaac-348">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0eaac-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0eaac-349">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0eaac-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0eaac-350">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0eaac-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0eaac-351">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="0eaac-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-352">Az.Sql</span></span>
* <span data-ttu-id="0eaac-353">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0eaac-354">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="0eaac-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eaac-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-355">Az.Websites</span></span>
* <span data-ttu-id="0eaac-356">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0eaac-357">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eaac-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-358">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-359">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="0eaac-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0eaac-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-360">Az.AnalysisServices</span></span>
<span data-ttu-id="0eaac-361">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="0eaac-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-362">Az.Compute</span></span>
* <span data-ttu-id="0eaac-363">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0eaac-364">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0eaac-365">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-366">Az.RecoveryServices</span></span>
<span data-ttu-id="0eaac-367">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="0eaac-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-368">Az.Resources</span></span>
* <span data-ttu-id="0eaac-369">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0eaac-370">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0eaac-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0eaac-371">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0eaac-372">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0eaac-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-373">Az.Sql</span></span>
* <span data-ttu-id="0eaac-374">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0eaac-375">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="0eaac-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0eaac-376">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0eaac-377">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eaac-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-378">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-379">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0eaac-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0eaac-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="0eaac-381">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="0eaac-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eaac-383">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="0eaac-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0eaac-384">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eaac-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-385">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-386">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eaac-387">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eaac-388">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0eaac-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0eaac-389">Az.Aks</span></span>
* <span data-ttu-id="0eaac-390">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eaac-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eaac-391">Az.Automation</span></span>
* <span data-ttu-id="0eaac-392">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0eaac-393">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eaac-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eaac-394">Az.Cdn</span></span>
* <span data-ttu-id="0eaac-395">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-396">Az.Compute</span></span>
* <span data-ttu-id="0eaac-397">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0eaac-398">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0eaac-399">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0eaac-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eaac-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0eaac-401">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eaac-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eaac-402">Az.DataFactory</span></span>
* <span data-ttu-id="0eaac-403">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eaac-405">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0eaac-406">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0eaac-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0eaac-407">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eaac-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eaac-408">Az.IotHub</span></span>
* <span data-ttu-id="0eaac-409">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eaac-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eaac-410">Az.KeyVault</span></span>
* <span data-ttu-id="0eaac-411">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-412">Az.Network</span></span>
* <span data-ttu-id="0eaac-413">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-414">Az.Resources</span></span>
* <span data-ttu-id="0eaac-415">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0eaac-416">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="0eaac-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0eaac-417">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="0eaac-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0eaac-418">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0eaac-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0eaac-419">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0eaac-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0eaac-420">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0eaac-421">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0eaac-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eaac-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eaac-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eaac-423">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0eaac-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0eaac-424">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-424">Fix some error messages.</span></span>
* <span data-ttu-id="0eaac-425">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="0eaac-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0eaac-426">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="0eaac-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0eaac-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0eaac-427">Az.SignalR</span></span>
* <span data-ttu-id="0eaac-428">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-429">Az.Sql</span></span>
* <span data-ttu-id="0eaac-430">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eaac-431">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0eaac-432">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="0eaac-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0eaac-433">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="0eaac-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eaac-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-434">Az.Storage</span></span>
* <span data-ttu-id="0eaac-435">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eaac-436">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0eaac-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0eaac-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0eaac-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0eaac-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0eaac-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0eaac-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0eaac-439">Az.TrafficManager</span></span>
* <span data-ttu-id="0eaac-440">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eaac-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-441">Az.Websites</span></span>
* <span data-ttu-id="0eaac-442">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eaac-443">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="0eaac-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0eaac-444">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0eaac-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0eaac-445">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="0eaac-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eaac-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-446">Az.Accounts</span></span>
* <span data-ttu-id="0eaac-447">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-448">Az.Compute</span></span>
* <span data-ttu-id="0eaac-449">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="0eaac-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0eaac-450">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0eaac-451">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eaac-453">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="0eaac-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0eaac-454">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0eaac-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0eaac-455">Az.EventGrid</span></span>
* <span data-ttu-id="0eaac-456">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0eaac-457">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0eaac-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0eaac-458">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0eaac-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0eaac-459">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="0eaac-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0eaac-460">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0eaac-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0eaac-461">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0eaac-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0eaac-462">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="0eaac-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0eaac-463">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="0eaac-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0eaac-464">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0eaac-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0eaac-465">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0eaac-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="0eaac-466">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0eaac-467">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="0eaac-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eaac-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eaac-468">Az.IotHub</span></span>
* <span data-ttu-id="0eaac-469">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eaac-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eaac-470">Az.LogicApp</span></span>
* <span data-ttu-id="0eaac-471">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="0eaac-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-472">Az.Resources</span></span>
* <span data-ttu-id="0eaac-473">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0eaac-474">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0eaac-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0eaac-475">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0eaac-476">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0eaac-477">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="0eaac-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0eaac-478">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0eaac-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0eaac-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0eaac-479">Az.SignalR</span></span>
* <span data-ttu-id="0eaac-480">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-481">Az.Sql</span></span>
* <span data-ttu-id="0eaac-482">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eaac-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-483">Az.Storage</span></span>
* <span data-ttu-id="0eaac-484">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0eaac-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0eaac-485">New-AzStorageContext</span></span>
* <span data-ttu-id="0eaac-486">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="0eaac-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0eaac-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0eaac-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eaac-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-488">Az.Websites</span></span>
* <span data-ttu-id="0eaac-489">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0eaac-490">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0eaac-491">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0eaac-492">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0eaac-492">General</span></span>

- <span data-ttu-id="0eaac-493">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="0eaac-493">General Availability of Az Module</span></span>
- <span data-ttu-id="0eaac-494">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="0eaac-494">Online help for each module</span></span>
- <span data-ttu-id="0eaac-495">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="0eaac-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0eaac-496">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0eaac-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eaac-497">Az.Accounts</span></span>
- <span data-ttu-id="0eaac-498">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eaac-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="0eaac-499">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="0eaac-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0eaac-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eaac-500">Az.ApiManagement</span></span>
- <span data-ttu-id="0eaac-501">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="0eaac-501">Fixes for #7002</span></span>
- <span data-ttu-id="0eaac-502">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0eaac-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eaac-503">Az.Batch</span></span>
- <span data-ttu-id="0eaac-504">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0eaac-505">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="0eaac-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0eaac-506">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0eaac-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0eaac-507">Az.Billing</span></span>
- <span data-ttu-id="0eaac-508">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0eaac-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-509">Az.CognitivServices</span></span>
- <span data-ttu-id="0eaac-510">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0eaac-511">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="0eaac-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0eaac-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="0eaac-513">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0eaac-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0eaac-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0eaac-515">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="0eaac-517">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0eaac-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eaac-518">Az.Monitor</span></span>
- <span data-ttu-id="0eaac-519">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0eaac-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eaac-520">Az.KeyVault</span></span>
- <span data-ttu-id="0eaac-521">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="0eaac-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0eaac-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0eaac-522">Az.MachineLearning</span></span>
- <span data-ttu-id="0eaac-523">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="0eaac-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0eaac-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0eaac-524">Az.Media</span></span>
- <span data-ttu-id="0eaac-525">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="0eaac-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0eaac-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-526">Az.Network</span></span>
<span data-ttu-id="0eaac-527">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0eaac-528">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0eaac-528">New cmdlets added:</span></span>
        - <span data-ttu-id="0eaac-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eaac-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eaac-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eaac-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eaac-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eaac-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eaac-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eaac-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eaac-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eaac-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eaac-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0eaac-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0eaac-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0eaac-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0eaac-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eaac-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0eaac-537">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0eaac-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0eaac-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0eaac-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0eaac-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0eaac-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0eaac-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0eaac-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eaac-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0eaac-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0eaac-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0eaac-543">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0eaac-544">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0eaac-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0eaac-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0eaac-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0eaac-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0eaac-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0eaac-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0eaac-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0eaac-548">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0eaac-549">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0eaac-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eaac-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="0eaac-551">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0eaac-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eaac-552">Az.Profile</span></span>
- <span data-ttu-id="0eaac-553">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="0eaac-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="0eaac-555">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0eaac-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-556">Az.Resources</span></span>
- <span data-ttu-id="0eaac-557">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0eaac-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eaac-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="0eaac-559">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="0eaac-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0eaac-560">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0eaac-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0eaac-561">Az.SIgnalR</span></span>
- <span data-ttu-id="0eaac-562">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0eaac-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0eaac-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-563">Az.Sql</span></span>
- <span data-ttu-id="0eaac-564">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0eaac-565">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0eaac-566">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0eaac-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-567">Az.Storage</span></span>
- <span data-ttu-id="0eaac-568">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0eaac-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-569">Az.Websites</span></span>
- <span data-ttu-id="0eaac-570">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0eaac-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0eaac-571">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0eaac-572">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0eaac-572">General</span></span>

* <span data-ttu-id="0eaac-573">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="0eaac-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0eaac-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-574">Az.Compute</span></span>

* <span data-ttu-id="0eaac-575">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="0eaac-577">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0eaac-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eaac-578">Az.FrontDoor</span></span>

* <span data-ttu-id="0eaac-579">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-579">Fixed some broken links</span></span>
    - <span data-ttu-id="0eaac-580">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0eaac-581">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0eaac-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="0eaac-583">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0eaac-584">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="0eaac-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0eaac-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-585">Az.Resources</span></span>

* <span data-ttu-id="0eaac-586">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0eaac-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0eaac-587">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0eaac-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0eaac-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-588">Az.Sql</span></span>

* <span data-ttu-id="0eaac-589">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="0eaac-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0eaac-590">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0eaac-591">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0eaac-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-592">Az.Storage</span></span>

* <span data-ttu-id="0eaac-593">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0eaac-594">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0eaac-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0eaac-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0eaac-596">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="0eaac-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0eaac-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0eaac-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0eaac-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0eaac-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-599">Az.Websites</span></span>

* <span data-ttu-id="0eaac-600">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0eaac-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0eaac-601">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0eaac-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0eaac-602">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="0eaac-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0eaac-603">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0eaac-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eaac-604">Az.ApiManagement</span></span>
* <span data-ttu-id="0eaac-605">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0eaac-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eaac-606">Az.Automation</span></span>
* <span data-ttu-id="0eaac-607">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0eaac-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0eaac-608">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0eaac-609">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0eaac-610">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0eaac-611">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0eaac-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-612">Az.Compute</span></span>
* <span data-ttu-id="0eaac-613">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0eaac-614">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0eaac-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="0eaac-616">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0eaac-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0eaac-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0eaac-618">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0eaac-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-619">Az.Network</span></span>
* <span data-ttu-id="0eaac-620">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0eaac-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0eaac-621">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0eaac-622">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0eaac-623">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0eaac-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0eaac-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0eaac-625">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0eaac-626">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="0eaac-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0eaac-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0eaac-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0eaac-628">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="0eaac-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0eaac-629">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0eaac-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0eaac-630">Az.Relay</span></span>
* <span data-ttu-id="0eaac-631">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="0eaac-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0eaac-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-632">Az.Resources</span></span>
* <span data-ttu-id="0eaac-633">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0eaac-634">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="0eaac-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0eaac-635">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0eaac-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0eaac-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eaac-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eaac-637">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0eaac-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-638">Az.Sql</span></span>
* <span data-ttu-id="0eaac-639">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0eaac-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eaac-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eaac-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eaac-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eaac-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eaac-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eaac-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0eaac-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eaac-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0eaac-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eaac-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0eaac-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eaac-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0eaac-648">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="0eaac-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0eaac-649">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="0eaac-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0eaac-650">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="0eaac-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0eaac-651">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="0eaac-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0eaac-652">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="0eaac-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0eaac-653">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0eaac-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0eaac-654">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0eaac-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0eaac-655">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0eaac-656">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0eaac-657">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0eaac-657">General</span></span>
* <span data-ttu-id="0eaac-658">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="0eaac-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0eaac-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eaac-659">Az.Profile</span></span>
* <span data-ttu-id="0eaac-660">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0eaac-661">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0eaac-662">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0eaac-663">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0eaac-664">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0eaac-665">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0eaac-666">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="0eaac-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eaac-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eaac-668">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-669">Az.Compute</span></span>
* <span data-ttu-id="0eaac-670">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0eaac-671">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="0eaac-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0eaac-672">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="0eaac-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eaac-674">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="0eaac-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0eaac-675">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0eaac-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0eaac-676">Az.Insights</span></span>
* <span data-ttu-id="0eaac-677">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="0eaac-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0eaac-678">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="0eaac-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0eaac-679">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0eaac-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0eaac-680">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-681">Az.Network</span></span>
* <span data-ttu-id="0eaac-682">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0eaac-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0eaac-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eaac-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0eaac-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0eaac-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0eaac-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0eaac-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0eaac-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0eaac-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0eaac-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eaac-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0eaac-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0eaac-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0eaac-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0eaac-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="0eaac-690">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-691">Az.Resources</span></span>
* <span data-ttu-id="0eaac-692">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0eaac-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0eaac-693">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="0eaac-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eaac-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eaac-694">Az.ServiceBus</span></span>
* <span data-ttu-id="0eaac-695">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="0eaac-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eaac-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eaac-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eaac-697">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0eaac-698">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="0eaac-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0eaac-699">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="0eaac-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0eaac-700">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="0eaac-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0eaac-701">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0eaac-702">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0eaac-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eaac-703">Az.Profile</span></span>
* <span data-ttu-id="0eaac-704">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0eaac-705">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-706">Az.Compute</span></span>
* <span data-ttu-id="0eaac-707">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="0eaac-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0eaac-708">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eaac-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eaac-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eaac-710">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0eaac-711">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0eaac-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0eaac-712">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="0eaac-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0eaac-713">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="0eaac-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0eaac-714">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0eaac-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-715">Az.Network</span></span>
* <span data-ttu-id="0eaac-716">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="0eaac-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0eaac-717">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-718">Az.Resources</span></span>
* <span data-ttu-id="0eaac-719">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0eaac-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0eaac-720">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0eaac-721">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0eaac-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0eaac-722">Azure.Storage</span></span>
* <span data-ttu-id="0eaac-723">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="0eaac-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0eaac-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0eaac-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0eaac-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0eaac-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0eaac-726">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="0eaac-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0eaac-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0eaac-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0eaac-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eaac-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eaac-729">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eaac-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eaac-730">Az.Compute</span></span>
* <span data-ttu-id="0eaac-731">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="0eaac-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0eaac-732">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0eaac-733">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="0eaac-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0eaac-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0eaac-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0eaac-735">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0eaac-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eaac-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eaac-736">Az.Network</span></span>
* <span data-ttu-id="0eaac-737">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0eaac-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0eaac-738">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-738">new cmdlets added</span></span>
    - <span data-ttu-id="0eaac-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eaac-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eaac-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eaac-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eaac-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eaac-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eaac-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eaac-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eaac-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0eaac-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0eaac-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0eaac-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0eaac-745">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0eaac-746">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0eaac-747">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0eaac-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0eaac-748">Az.RedisCache</span></span>
* <span data-ttu-id="0eaac-749">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="0eaac-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0eaac-750">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eaac-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eaac-751">Az.Resources</span></span>
* <span data-ttu-id="0eaac-752">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0eaac-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0eaac-753">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="0eaac-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eaac-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eaac-754">Az.Sql</span></span>
* <span data-ttu-id="0eaac-755">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="0eaac-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eaac-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eaac-756">Az.Websites</span></span>
* <span data-ttu-id="0eaac-757">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="0eaac-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0eaac-758">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="0eaac-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0eaac-759">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="0eaac-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0eaac-760">Erste Version</span><span class="sxs-lookup"><span data-stu-id="0eaac-760">Initial Release</span></span>