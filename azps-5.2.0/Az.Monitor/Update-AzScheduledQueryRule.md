---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297058"
---
# <span data-ttu-id="0eabe-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0eabe-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="0eabe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eabe-102">SYNOPSIS</span></span>
<span data-ttu-id="0eabe-103">Aktualisiert eine Protokollbenachrichtigungsregel</span><span class="sxs-lookup"><span data-stu-id="0eabe-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="0eabe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0eabe-104">SYNTAX</span></span>

### <span data-ttu-id="0eabe-105">ByRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0eabe-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eabe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0eabe-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eabe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0eabe-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eabe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0eabe-108">DESCRIPTION</span></span>
<span data-ttu-id="0eabe-109">Aktualisiert eine Protokollwarnungsregel, und das Aktualisieren nur der Eigenschaft "Enabled" wird von diesem Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0eabe-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="0eabe-110">Informationen zum Aktualisieren anderer Eigenschaften finden Sie unter ["Set-AzScheduledQueryRule".](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule)</span><span class="sxs-lookup"><span data-stu-id="0eabe-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="0eabe-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0eabe-111">EXAMPLES</span></span>

### <span data-ttu-id="0eabe-112">Beispiel 1: Aktualisieren nach Regelname</span><span class="sxs-lookup"><span data-stu-id="0eabe-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="0eabe-113">Beispiel 2: Aktualisieren nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="0eabe-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="0eabe-114">Beispiel 3: Aktualisieren nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0eabe-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="0eabe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eabe-115">PARAMETERS</span></span>

### <span data-ttu-id="0eabe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eabe-116">-DefaultProfile</span></span>
<span data-ttu-id="0eabe-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0eabe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eabe-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="0eabe-118">-Enabled</span></span>
<span data-ttu-id="0eabe-119">Der Azure Alert State – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="0eabe-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eabe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eabe-120">-InputObject</span></span>
<span data-ttu-id="0eabe-121">Ressource "Geplante Abfrageregel"</span><span class="sxs-lookup"><span data-stu-id="0eabe-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eabe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0eabe-122">-Name</span></span>
<span data-ttu-id="0eabe-123">Der Benachrichtigungsname</span><span class="sxs-lookup"><span data-stu-id="0eabe-123">The alert name</span></span>

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

### <span data-ttu-id="0eabe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eabe-124">-ResourceGroupName</span></span>
<span data-ttu-id="0eabe-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0eabe-125">The resource group name</span></span>

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

### <span data-ttu-id="0eabe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eabe-126">-ResourceId</span></span>
<span data-ttu-id="0eabe-127">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0eabe-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eabe-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eabe-128">-Confirm</span></span>
<span data-ttu-id="0eabe-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0eabe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eabe-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0eabe-130">-WhatIf</span></span>
<span data-ttu-id="0eabe-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0eabe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eabe-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0eabe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eabe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eabe-133">CommonParameters</span></span>
<span data-ttu-id="0eabe-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eabe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eabe-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eabe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eabe-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0eabe-136">INPUTS</span></span>

### <span data-ttu-id="0eabe-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0eabe-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="0eabe-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0eabe-138">System.String</span></span>

## <span data-ttu-id="0eabe-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0eabe-139">OUTPUTS</span></span>

### <span data-ttu-id="0eabe-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0eabe-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="0eabe-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0eabe-141">NOTES</span></span>

## <span data-ttu-id="0eabe-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0eabe-142">RELATED LINKS</span></span>
