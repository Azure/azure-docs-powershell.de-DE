---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925483"
---
# <span data-ttu-id="d8cc4-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="d8cc4-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="d8cc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cc4-103">Erstellt eine Lösung für die Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="d8cc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8cc4-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8cc4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cc4-106">Erstellt eine Lösung für die Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="d8cc4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="d8cc4-108">Beispiel 1: Erstellen einer Lösung für die Überwachungsprotokollanalyse für den Protokollanalysearbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d8cc4-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="d8cc4-109">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse für den Protokollanalysearbeitsbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="d8cc4-110">Häufig verwendete Typen sind:</span><span class="sxs-lookup"><span data-stu-id="d8cc4-110">Commonly used types are:</span></span>

| <span data-ttu-id="d8cc4-111">Typ</span><span class="sxs-lookup"><span data-stu-id="d8cc4-111">Type</span></span> | <span data-ttu-id="d8cc4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8cc4-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="d8cc4-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="d8cc4-113">SecurityCenterFree</span></span> |  <span data-ttu-id="d8cc4-114">Azure Security Center – Free Edition</span><span class="sxs-lookup"><span data-stu-id="d8cc4-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="d8cc4-115">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d8cc4-115">Security</span></span> | <span data-ttu-id="d8cc4-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="d8cc4-116">Azure Security Center</span></span> |
| <span data-ttu-id="d8cc4-117">Updates</span><span class="sxs-lookup"><span data-stu-id="d8cc4-117">Updates</span></span> | <span data-ttu-id="d8cc4-118">Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="d8cc4-118">Update Management</span></span> |
| <span data-ttu-id="d8cc4-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="d8cc4-119">ContainerInsights</span></span> | <span data-ttu-id="d8cc4-120">Azure Monitor für Container</span><span class="sxs-lookup"><span data-stu-id="d8cc4-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="d8cc4-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="d8cc4-121">ServiceMap</span></span> | <span data-ttu-id="d8cc4-122">Dienstzuordnung</span><span class="sxs-lookup"><span data-stu-id="d8cc4-122">Service Map</span></span> |
| <span data-ttu-id="d8cc4-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="d8cc4-123">AzureActivity</span></span> | <span data-ttu-id="d8cc4-124">Aktivitätsprotokollanalyse</span><span class="sxs-lookup"><span data-stu-id="d8cc4-124">Activity log analytics</span></span> |
| <span data-ttu-id="d8cc4-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="d8cc4-125">ChangeTracking</span></span> | <span data-ttu-id="d8cc4-126">Ändern von Nachverfolgung und Bestand</span><span class="sxs-lookup"><span data-stu-id="d8cc4-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="d8cc4-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="d8cc4-127">VMInsights</span></span> | <span data-ttu-id="d8cc4-128">Azure Monitor für VMs</span><span class="sxs-lookup"><span data-stu-id="d8cc4-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="d8cc4-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="d8cc4-129">SecurityInsights</span></span> | <span data-ttu-id="d8cc4-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="d8cc4-130">Azure Sentinel</span></span> |
| <span data-ttu-id="d8cc4-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="d8cc4-131">NetworkMonitoring</span></span> | <span data-ttu-id="d8cc4-132">Netzwerkleistungsmonitor</span><span class="sxs-lookup"><span data-stu-id="d8cc4-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="d8cc4-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="d8cc4-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="d8cc4-134">SQL Sicherheitsrisikobeurteilung</span><span class="sxs-lookup"><span data-stu-id="d8cc4-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="d8cc4-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="d8cc4-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="d8cc4-136">SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d8cc4-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="d8cc4-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="d8cc4-137">AntiMalware</span></span> | <span data-ttu-id="d8cc4-138">Antimalware-Bewertung</span><span class="sxs-lookup"><span data-stu-id="d8cc4-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="d8cc4-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="d8cc4-139">AzureAutomation</span></span> | <span data-ttu-id="d8cc4-140">Automatisierungs-Hybridarbeiter</span><span class="sxs-lookup"><span data-stu-id="d8cc4-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="d8cc4-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="d8cc4-141">LogicAppsManagement</span></span> | <span data-ttu-id="d8cc4-142">Verwaltung von Logik-Apps</span><span class="sxs-lookup"><span data-stu-id="d8cc4-142">Logic Apps Management</span></span> |
| <span data-ttu-id="d8cc4-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="d8cc4-143">SQLDataClassification</span></span> | <span data-ttu-id="d8cc4-144">SQL Data Discovery & Classification</span><span class="sxs-lookup"><span data-stu-id="d8cc4-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="d8cc4-145">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8cc4-145">PARAMETERS</span></span>

### <span data-ttu-id="d8cc4-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cc4-146">-DefaultProfile</span></span>
<span data-ttu-id="d8cc4-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8cc4-148">-Location</span><span class="sxs-lookup"><span data-stu-id="d8cc4-148">-Location</span></span>
<span data-ttu-id="d8cc4-149">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-149">Resource location.</span></span>
<span data-ttu-id="d8cc4-150">Muss mit dem Protokollanalysearbeitsbereich identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="d8cc4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cc4-151">-ResourceGroupName</span></span>
<span data-ttu-id="d8cc4-152">Der Name der zu erhaltende Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-152">The name of the resource group to get.</span></span>
<span data-ttu-id="d8cc4-153">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d8cc4-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8cc4-154">-SubscriptionId</span></span>
<span data-ttu-id="d8cc4-155">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8cc4-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8cc4-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8cc4-157">-Tag</span></span>
<span data-ttu-id="d8cc4-158">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="d8cc4-158">Resource tags</span></span>

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

### <span data-ttu-id="d8cc4-159">-Type</span><span class="sxs-lookup"><span data-stu-id="d8cc4-159">-Type</span></span>
<span data-ttu-id="d8cc4-160">Typ der zu erstellende Lösung.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-160">Type of the solution to be created.</span></span>
<span data-ttu-id="d8cc4-161">Beispiel: "Container".</span><span class="sxs-lookup"><span data-stu-id="d8cc4-161">For example "Container".</span></span>

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

### <span data-ttu-id="d8cc4-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d8cc4-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="d8cc4-163">Die Azure-Ressourcen-ID für den Arbeitsbereich, in dem die Projektmappe bereitgestellt/aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="d8cc4-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8cc4-164">-Confirm</span></span>
<span data-ttu-id="d8cc4-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8cc4-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8cc4-166">-WhatIf</span></span>
<span data-ttu-id="d8cc4-167">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8cc4-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8cc4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cc4-169">CommonParameters</span></span>
<span data-ttu-id="d8cc4-170">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cc4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cc4-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8cc4-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cc4-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8cc4-172">INPUTS</span></span>

## <span data-ttu-id="d8cc4-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8cc4-173">OUTPUTS</span></span>

### <span data-ttu-id="d8cc4-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="d8cc4-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="d8cc4-175">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d8cc4-175">NOTES</span></span>

<span data-ttu-id="d8cc4-176">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d8cc4-176">ALIASES</span></span>

## <span data-ttu-id="d8cc4-177">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d8cc4-177">RELATED LINKS</span></span>



[<span data-ttu-id="d8cc4-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8cc4-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

