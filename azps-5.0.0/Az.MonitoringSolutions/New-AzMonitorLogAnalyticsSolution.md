---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179611"
---
# <span data-ttu-id="5ca04-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="5ca04-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="5ca04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ca04-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca04-103">Erstellt eine Protokollanalyse Lösung.</span><span class="sxs-lookup"><span data-stu-id="5ca04-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="5ca04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ca04-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ca04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ca04-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca04-106">Erstellt eine Protokollanalyse Lösung.</span><span class="sxs-lookup"><span data-stu-id="5ca04-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="5ca04-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ca04-107">EXAMPLES</span></span>

### <span data-ttu-id="5ca04-108">Beispiel 1: Erstellen einer Überwachungsprotokoll Analyse-Lösung für den Arbeitsbereich "Protokollanalyse"</span><span class="sxs-lookup"><span data-stu-id="5ca04-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="5ca04-109">Mit diesem Befehl wird eine Überwachungsprotokoll Analyse Lösung für den Arbeitsbereich "Protokollanalyse" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ca04-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="5ca04-110">Häufig verwendete Typen sind:</span><span class="sxs-lookup"><span data-stu-id="5ca04-110">Commonly used types are:</span></span>

| <span data-ttu-id="5ca04-111">Geben</span><span class="sxs-lookup"><span data-stu-id="5ca04-111">Type</span></span> | <span data-ttu-id="5ca04-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ca04-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="5ca04-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="5ca04-113">SecurityCenterFree</span></span> |  <span data-ttu-id="5ca04-114">Azure Security Center – ﻿kostenlose Edition</span><span class="sxs-lookup"><span data-stu-id="5ca04-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="5ca04-115">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="5ca04-115">Security</span></span> | <span data-ttu-id="5ca04-116">Azure-Sicherheits Center</span><span class="sxs-lookup"><span data-stu-id="5ca04-116">Azure Security Center</span></span> |
| <span data-ttu-id="5ca04-117">Updates</span><span class="sxs-lookup"><span data-stu-id="5ca04-117">Updates</span></span> | <span data-ttu-id="5ca04-118">Update Verwaltung</span><span class="sxs-lookup"><span data-stu-id="5ca04-118">Update Management</span></span> |
| <span data-ttu-id="5ca04-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="5ca04-119">ContainerInsights</span></span> | <span data-ttu-id="5ca04-120">Azure Monitor für Container</span><span class="sxs-lookup"><span data-stu-id="5ca04-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="5ca04-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="5ca04-121">ServiceMap</span></span> | <span data-ttu-id="5ca04-122">Service Karte</span><span class="sxs-lookup"><span data-stu-id="5ca04-122">Service Map</span></span> |
| <span data-ttu-id="5ca04-123">Azure</span><span class="sxs-lookup"><span data-stu-id="5ca04-123">AzureActivity</span></span> | <span data-ttu-id="5ca04-124">Aktivitätsprotokoll Analyse</span><span class="sxs-lookup"><span data-stu-id="5ca04-124">Activity log analytics</span></span> |
| <span data-ttu-id="5ca04-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="5ca04-125">ChangeTracking</span></span> | <span data-ttu-id="5ca04-126">Änderungsnachverfolgung und Inventar</span><span class="sxs-lookup"><span data-stu-id="5ca04-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="5ca04-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="5ca04-127">VMInsights</span></span> | <span data-ttu-id="5ca04-128">Azure Monitor für VMS</span><span class="sxs-lookup"><span data-stu-id="5ca04-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="5ca04-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="5ca04-129">SecurityInsights</span></span> | <span data-ttu-id="5ca04-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="5ca04-130">Azure Sentinel</span></span> |
| <span data-ttu-id="5ca04-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="5ca04-131">NetworkMonitoring</span></span> | <span data-ttu-id="5ca04-132">Netzwerk Leistungs Monitor</span><span class="sxs-lookup"><span data-stu-id="5ca04-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="5ca04-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="5ca04-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="5ca04-134">SQL-Anfälligkeitsbewertung</span><span class="sxs-lookup"><span data-stu-id="5ca04-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="5ca04-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5ca04-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="5ca04-136">Erweiterter SQL-Bedrohungsschutz</span><span class="sxs-lookup"><span data-stu-id="5ca04-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="5ca04-137">Antischadsoftware</span><span class="sxs-lookup"><span data-stu-id="5ca04-137">AntiMalware</span></span> | <span data-ttu-id="5ca04-138">Antimalware-Bewertung</span><span class="sxs-lookup"><span data-stu-id="5ca04-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="5ca04-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="5ca04-139">AzureAutomation</span></span> | <span data-ttu-id="5ca04-140">Automatisierungs-Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="5ca04-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="5ca04-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="5ca04-141">LogicAppsManagement</span></span> | <span data-ttu-id="5ca04-142">Verwaltung von Logic-apps</span><span class="sxs-lookup"><span data-stu-id="5ca04-142">Logic Apps Management</span></span> |
| <span data-ttu-id="5ca04-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="5ca04-143">SQLDataClassification</span></span> | <span data-ttu-id="5ca04-144">SQL-Daten Ermittlungs & Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="5ca04-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="5ca04-145">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ca04-145">PARAMETERS</span></span>

### <span data-ttu-id="5ca04-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca04-146">-DefaultProfile</span></span>
<span data-ttu-id="5ca04-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ca04-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-148">-Standort</span><span class="sxs-lookup"><span data-stu-id="5ca04-148">-Location</span></span>
<span data-ttu-id="5ca04-149">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="5ca04-149">Resource location.</span></span>
<span data-ttu-id="5ca04-150">Muss derselbe wie der Protokollanalyse-Arbeitsbereich sein.</span><span class="sxs-lookup"><span data-stu-id="5ca04-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca04-151">-ResourceGroupName</span></span>
<span data-ttu-id="5ca04-152">Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ca04-152">The name of the resource group to get.</span></span>
<span data-ttu-id="5ca04-153">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5ca04-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-154">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5ca04-154">-SubscriptionId</span></span>
<span data-ttu-id="5ca04-155">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5ca04-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ca04-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5ca04-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ca04-157">-Tag</span></span>
<span data-ttu-id="5ca04-158">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="5ca04-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-159">-Typ</span><span class="sxs-lookup"><span data-stu-id="5ca04-159">-Type</span></span>
<span data-ttu-id="5ca04-160">Der Typ der zu erstellende Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="5ca04-160">Type of the solution to be created.</span></span>
<span data-ttu-id="5ca04-161">Beispiel: "Container".</span><span class="sxs-lookup"><span data-stu-id="5ca04-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca04-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="5ca04-163">Die Azure-Ressourcen-ID für den Arbeitsbereich, in dem die Lösung bereitgestellt/aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="5ca04-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ca04-164">-Confirm</span></span>
<span data-ttu-id="5ca04-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ca04-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca04-166">-WhatIf</span></span>
<span data-ttu-id="5ca04-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ca04-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ca04-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ca04-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca04-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca04-169">CommonParameters</span></span>
<span data-ttu-id="5ca04-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca04-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca04-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ca04-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca04-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ca04-172">INPUTS</span></span>

## <span data-ttu-id="5ca04-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ca04-173">OUTPUTS</span></span>

### <span data-ttu-id="5ca04-174">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="5ca04-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="5ca04-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ca04-175">NOTES</span></span>

<span data-ttu-id="5ca04-176">Aliase</span><span class="sxs-lookup"><span data-stu-id="5ca04-176">ALIASES</span></span>

## <span data-ttu-id="5ca04-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ca04-177">RELATED LINKS</span></span>



[<span data-ttu-id="5ca04-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ca04-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

