---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159857"
---
# <span data-ttu-id="a86be-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="a86be-101">Get-AzActionRule</span></span>

## <span data-ttu-id="a86be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a86be-102">SYNOPSIS</span></span>
<span data-ttu-id="a86be-103">Informationen zu Aktionsregeln</span><span class="sxs-lookup"><span data-stu-id="a86be-103">Get Action Rules Information</span></span>

## <span data-ttu-id="a86be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a86be-104">SYNTAX</span></span>

### <span data-ttu-id="a86be-105">ListActionRules (Standard)</span><span class="sxs-lookup"><span data-stu-id="a86be-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a86be-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a86be-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a86be-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="a86be-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a86be-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a86be-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a86be-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a86be-109">DESCRIPTION</span></span>
<span data-ttu-id="a86be-110">**Beim Get-AzActionRule-Cmdlet** werden Aktionsregeln konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a86be-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="a86be-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a86be-111">EXAMPLES</span></span>

### <span data-ttu-id="a86be-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a86be-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="a86be-113">Listen Sie alle in der Ressourcengruppe konfigurierten Aktionsregeln auf, die nach dem Schweregrad "Sev2" und dem Dienst für die Plattformüberwachung gefiltert sind.</span><span class="sxs-lookup"><span data-stu-id="a86be-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="a86be-114">Verwenden Format-List, um die Details jeder Aktionsregel in der Liste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a86be-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="a86be-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a86be-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="a86be-116">Sie erhalten die Aktionsregel mit dem Namen "Test-Action-Rule" in der Ressourcengruppe "test-rg".</span><span class="sxs-lookup"><span data-stu-id="a86be-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="a86be-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a86be-117">PARAMETERS</span></span>

### <span data-ttu-id="a86be-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="a86be-118">-ActionGroup</span></span>
<span data-ttu-id="a86be-119">Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="a86be-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a86be-120">-AlertRuleId</span></span>
<span data-ttu-id="a86be-121">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="a86be-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86be-122">-DefaultProfile</span></span>
<span data-ttu-id="a86be-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a86be-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a86be-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a86be-124">-Description</span></span>
<span data-ttu-id="a86be-125">Filtern aller Benachrichtigungen mit der Intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="a86be-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="a86be-126">-ImpactedScope</span></span>
<span data-ttu-id="a86be-127">Filtern nach "Betroffener Bereich"</span><span class="sxs-lookup"><span data-stu-id="a86be-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="a86be-128">-MonitorService</span></span>
<span data-ttu-id="a86be-129">Filtern nach Moniter Service</span><span class="sxs-lookup"><span data-stu-id="a86be-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a86be-130">-Name</span></span>
<span data-ttu-id="a86be-131">Name der Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="a86be-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86be-132">-ResourceGroupName</span></span>
<span data-ttu-id="a86be-133">Ressourcengruppenname, in dem sich die Aktionsregel befindet.</span><span class="sxs-lookup"><span data-stu-id="a86be-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a86be-134">-ResourceId</span></span>
<span data-ttu-id="a86be-135">Aktionsregel nach Ressourcen-ID erhalten.</span><span class="sxs-lookup"><span data-stu-id="a86be-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-136">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="a86be-136">-Severity</span></span>
<span data-ttu-id="a86be-137">Filtern nach Schweregrad der Warnung</span><span class="sxs-lookup"><span data-stu-id="a86be-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a86be-138">-TargetResourceGroup</span></span>
<span data-ttu-id="a86be-139">Filtern Sie nach dem Namen der Ressourcengruppe der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="a86be-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a86be-140">-TargetResourceId</span></span>
<span data-ttu-id="a86be-141">Filtern Sie nach der Ressourcen-ID der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="a86be-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="a86be-142">-TargetResourceType</span></span>
<span data-ttu-id="a86be-143">Filtern Sie nach dem Ressourcentyp der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="a86be-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86be-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86be-144">CommonParameters</span></span>
<span data-ttu-id="a86be-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86be-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86be-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a86be-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86be-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a86be-147">INPUTS</span></span>

### <span data-ttu-id="a86be-148">Keine</span><span class="sxs-lookup"><span data-stu-id="a86be-148">None</span></span>

## <span data-ttu-id="a86be-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a86be-149">OUTPUTS</span></span>

### <span data-ttu-id="a86be-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="a86be-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="a86be-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a86be-151">NOTES</span></span>

## <span data-ttu-id="a86be-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a86be-152">RELATED LINKS</span></span>
