---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: d809a7d01e6b4d477a72d26df11d73e87678d7e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301928"
---
# <span data-ttu-id="7ecab-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ecab-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="7ecab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ecab-102">SYNOPSIS</span></span>
<span data-ttu-id="7ecab-103">Ruft metrische Warnungsregeln für V2 (nicht klassisch) ab</span><span class="sxs-lookup"><span data-stu-id="7ecab-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="7ecab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ecab-104">SYNTAX</span></span>

### <span data-ttu-id="7ecab-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ecab-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ecab-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="7ecab-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ecab-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="7ecab-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ecab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ecab-108">DESCRIPTION</span></span>
<span data-ttu-id="7ecab-109">Das **Cmdlet "Get-AzMetricAlertRuleV2"** ruft eine metrische Warnungsregel nach dem Namen oder URI oder allen metrischen Warnungsregeln aus einer angegebenen Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7ecab-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="7ecab-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ecab-110">EXAMPLES</span></span>

### <span data-ttu-id="7ecab-111">Beispiel 1: Alle metrischen Warnungsregeln im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="7ecab-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="7ecab-112">Dieser Befehl ruft alle metrischen Warnungsregeln im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7ecab-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="7ecab-113">Beispiel 2: Alle metrischen Warnungsregeln in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="7ecab-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="7ecab-114">Dieser Befehl ruft alle metrischen Warnungsregeln in der Ressourcengruppe mit dem Namen "metricAlertsRG" ab.</span><span class="sxs-lookup"><span data-stu-id="7ecab-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="7ecab-115">Beispiel 3: Erhalten einer metrischen Warnungsregel nach Name</span><span class="sxs-lookup"><span data-stu-id="7ecab-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="7ecab-116">Dieser Befehl ruft die metrische Warnungsregel namens PS3182019 in der Ressourcengruppe mit dem Namen "metricAlertsRG" ab.</span><span class="sxs-lookup"><span data-stu-id="7ecab-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="7ecab-117">Beispiel 4: Erhalten einer metrischen Warnungsregel nach Regel-ID</span><span class="sxs-lookup"><span data-stu-id="7ecab-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="7ecab-118">Dieser Befehl ruft die metrische Warnungsregel mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="7ecab-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="7ecab-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ecab-119">PARAMETERS</span></span>

### <span data-ttu-id="7ecab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ecab-120">-DefaultProfile</span></span>
<span data-ttu-id="7ecab-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ecab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7ecab-122">-Name</span></span>
<span data-ttu-id="7ecab-123">Der Name der metrischen Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="7ecab-123">The Name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ecab-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ecab-125">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ecab-125">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ecab-126">-ResourceId</span></span>
<span data-ttu-id="7ecab-127">Regel-ID der metrischen Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="7ecab-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ecab-128">CommonParameters</span></span>
<span data-ttu-id="7ecab-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ecab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ecab-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ecab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ecab-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ecab-131">INPUTS</span></span>

### <span data-ttu-id="7ecab-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7ecab-132">System.String</span></span>

## <span data-ttu-id="7ecab-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ecab-133">OUTPUTS</span></span>

### <span data-ttu-id="7ecab-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ecab-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="7ecab-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ecab-135">NOTES</span></span>

## <span data-ttu-id="7ecab-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ecab-136">RELATED LINKS</span></span>
