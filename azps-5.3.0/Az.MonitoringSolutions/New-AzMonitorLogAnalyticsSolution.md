---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458995"
---
# <span data-ttu-id="78297-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="78297-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="78297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78297-102">SYNOPSIS</span></span>
<span data-ttu-id="78297-103">Erstellt eine Protokollanalyselösung.</span><span class="sxs-lookup"><span data-stu-id="78297-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="78297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78297-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78297-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78297-105">DESCRIPTION</span></span>
<span data-ttu-id="78297-106">Erstellt eine Protokollanalyselösung.</span><span class="sxs-lookup"><span data-stu-id="78297-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="78297-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78297-107">EXAMPLES</span></span>

### <span data-ttu-id="78297-108">Beispiel 1: Erstellen einer Lösung für die Überwachungsprotokollanalyse für den Protokollanalysearbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="78297-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="78297-109">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse für den Protokollanalysearbeitsbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="78297-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="78297-110">Häufig verwendete Typen sind:</span><span class="sxs-lookup"><span data-stu-id="78297-110">Commonly used types are:</span></span>

| <span data-ttu-id="78297-111">Typ</span><span class="sxs-lookup"><span data-stu-id="78297-111">Type</span></span> | <span data-ttu-id="78297-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78297-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="78297-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="78297-113">SecurityCenterFree</span></span> |  <span data-ttu-id="78297-114">Azure Security Center – Free Edition</span><span class="sxs-lookup"><span data-stu-id="78297-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="78297-115">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="78297-115">Security</span></span> | <span data-ttu-id="78297-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="78297-116">Azure Security Center</span></span> |
| <span data-ttu-id="78297-117">Updates</span><span class="sxs-lookup"><span data-stu-id="78297-117">Updates</span></span> | <span data-ttu-id="78297-118">Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="78297-118">Update Management</span></span> |
| <span data-ttu-id="78297-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="78297-119">ContainerInsights</span></span> | <span data-ttu-id="78297-120">Azure Monitor for Containers</span><span class="sxs-lookup"><span data-stu-id="78297-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="78297-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="78297-121">ServiceMap</span></span> | <span data-ttu-id="78297-122">Service Map</span><span class="sxs-lookup"><span data-stu-id="78297-122">Service Map</span></span> |
| <span data-ttu-id="78297-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="78297-123">AzureActivity</span></span> | <span data-ttu-id="78297-124">Aktivitätsprotokollanalyse</span><span class="sxs-lookup"><span data-stu-id="78297-124">Activity log analytics</span></span> |
| <span data-ttu-id="78297-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="78297-125">ChangeTracking</span></span> | <span data-ttu-id="78297-126">Änderungsnachverfolgung und -bestand</span><span class="sxs-lookup"><span data-stu-id="78297-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="78297-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="78297-127">VMInsights</span></span> | <span data-ttu-id="78297-128">Azure Monitor für VMs</span><span class="sxs-lookup"><span data-stu-id="78297-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="78297-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="78297-129">SecurityInsights</span></span> | <span data-ttu-id="78297-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="78297-130">Azure Sentinel</span></span> |
| <span data-ttu-id="78297-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="78297-131">NetworkMonitoring</span></span> | <span data-ttu-id="78297-132">Netzwerkleistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="78297-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="78297-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="78297-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="78297-134">SQL Sicherheitsrisikobewertung</span><span class="sxs-lookup"><span data-stu-id="78297-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="78297-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="78297-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="78297-136">SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="78297-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="78297-137">Antischalware</span><span class="sxs-lookup"><span data-stu-id="78297-137">AntiMalware</span></span> | <span data-ttu-id="78297-138">Antimalwarebewertung</span><span class="sxs-lookup"><span data-stu-id="78297-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="78297-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="78297-139">AzureAutomation</span></span> | <span data-ttu-id="78297-140">Automatisierungs-Hybrid-Worker</span><span class="sxs-lookup"><span data-stu-id="78297-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="78297-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="78297-141">LogicAppsManagement</span></span> | <span data-ttu-id="78297-142">Logik-Apps-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="78297-142">Logic Apps Management</span></span> |
| <span data-ttu-id="78297-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="78297-143">SQLDataClassification</span></span> | <span data-ttu-id="78297-144">SQL Data Discovery & Classification</span><span class="sxs-lookup"><span data-stu-id="78297-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="78297-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78297-145">PARAMETERS</span></span>

### <span data-ttu-id="78297-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78297-146">-DefaultProfile</span></span>
<span data-ttu-id="78297-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78297-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78297-148">-Location</span><span class="sxs-lookup"><span data-stu-id="78297-148">-Location</span></span>
<span data-ttu-id="78297-149">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="78297-149">Resource location.</span></span>
<span data-ttu-id="78297-150">Muss mit dem Loganalysearbeitsbereich identisch sein.</span><span class="sxs-lookup"><span data-stu-id="78297-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="78297-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78297-151">-ResourceGroupName</span></span>
<span data-ttu-id="78297-152">Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="78297-152">The name of the resource group to get.</span></span>
<span data-ttu-id="78297-153">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="78297-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="78297-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78297-154">-SubscriptionId</span></span>
<span data-ttu-id="78297-155">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78297-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="78297-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="78297-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="78297-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="78297-157">-Tag</span></span>
<span data-ttu-id="78297-158">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="78297-158">Resource tags</span></span>

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

### <span data-ttu-id="78297-159">-Type</span><span class="sxs-lookup"><span data-stu-id="78297-159">-Type</span></span>
<span data-ttu-id="78297-160">Typ der zu erstellende Lösung.</span><span class="sxs-lookup"><span data-stu-id="78297-160">Type of the solution to be created.</span></span>
<span data-ttu-id="78297-161">Beispiel: "Container".</span><span class="sxs-lookup"><span data-stu-id="78297-161">For example "Container".</span></span>

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

### <span data-ttu-id="78297-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="78297-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="78297-163">Die Azure-Ressourcen-ID für den Arbeitsbereich, in dem die Lösung bereitgestellt/aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="78297-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="78297-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78297-164">-Confirm</span></span>
<span data-ttu-id="78297-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78297-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78297-166">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="78297-166">-WhatIf</span></span>
<span data-ttu-id="78297-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78297-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78297-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78297-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78297-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78297-169">CommonParameters</span></span>
<span data-ttu-id="78297-170">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78297-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78297-171">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78297-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78297-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78297-172">INPUTS</span></span>

## <span data-ttu-id="78297-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78297-173">OUTPUTS</span></span>

### <span data-ttu-id="78297-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="78297-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="78297-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78297-175">NOTES</span></span>

<span data-ttu-id="78297-176">ALIASE</span><span class="sxs-lookup"><span data-stu-id="78297-176">ALIASES</span></span>

## <span data-ttu-id="78297-177">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78297-177">RELATED LINKS</span></span>



[<span data-ttu-id="78297-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="78297-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

