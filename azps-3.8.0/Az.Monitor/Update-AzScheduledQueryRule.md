---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1d58fba402f292c0935fc10715e06b323353046c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845079"
---
# <span data-ttu-id="ffb84-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ffb84-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="ffb84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffb84-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb84-103">Aktualisiert eine Protokoll Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="ffb84-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="ffb84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb84-104">SYNTAX</span></span>

### <span data-ttu-id="ffb84-105">ByRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffb84-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb84-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ffb84-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb84-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffb84-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb84-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffb84-108">DESCRIPTION</span></span>
<span data-ttu-id="ffb84-109">Aktualisiert eine Protokoll Warnungsregel, die nur die "Enabled"-Eigenschaft aktualisiert, wird durch diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ffb84-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="ffb84-110">Informationen zum Aktualisieren weiterer Eigenschaften finden Sie unter Befehl "Satz-AzScheduledQueryRule".</span><span class="sxs-lookup"><span data-stu-id="ffb84-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="ffb84-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffb84-111">EXAMPLES</span></span>

### <span data-ttu-id="ffb84-112">Beispiel 1 – Aktualisieren des Regel namens</span><span class="sxs-lookup"><span data-stu-id="ffb84-112">Example 1 - Update by rule name</span></span>
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

### <span data-ttu-id="ffb84-113">Beispiel 2 – Update nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="ffb84-113">Example 2 - Update by input object</span></span>
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

### <span data-ttu-id="ffb84-114">Beispiel 3 – Update nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ffb84-114">Example 3 - Update by resource Id</span></span>
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

## <span data-ttu-id="ffb84-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffb84-115">PARAMETERS</span></span>

### <span data-ttu-id="ffb84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb84-116">-DefaultProfile</span></span>
<span data-ttu-id="ffb84-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffb84-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffb84-118">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ffb84-118">-Enabled</span></span>
<span data-ttu-id="ffb84-119">Der Azure-Warnungszustand – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="ffb84-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="ffb84-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ffb84-120">-InputObject</span></span>
<span data-ttu-id="ffb84-121">Die geplante Abfrageregel Ressource</span><span class="sxs-lookup"><span data-stu-id="ffb84-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="ffb84-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ffb84-122">-Name</span></span>
<span data-ttu-id="ffb84-123">Der Warnungsname</span><span class="sxs-lookup"><span data-stu-id="ffb84-123">The alert name</span></span>

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

### <span data-ttu-id="ffb84-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb84-124">-ResourceGroupName</span></span>
<span data-ttu-id="ffb84-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ffb84-125">The resource group name</span></span>

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

### <span data-ttu-id="ffb84-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ffb84-126">-ResourceId</span></span>
<span data-ttu-id="ffb84-127">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ffb84-127">The resource Id</span></span>

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

### <span data-ttu-id="ffb84-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffb84-128">-Confirm</span></span>
<span data-ttu-id="ffb84-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffb84-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb84-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb84-130">-WhatIf</span></span>
<span data-ttu-id="ffb84-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffb84-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb84-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffb84-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb84-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb84-133">CommonParameters</span></span>
<span data-ttu-id="ffb84-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb84-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb84-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffb84-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb84-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffb84-136">INPUTS</span></span>

### <span data-ttu-id="ffb84-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ffb84-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="ffb84-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ffb84-138">System.String</span></span>

## <span data-ttu-id="ffb84-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffb84-139">OUTPUTS</span></span>

### <span data-ttu-id="ffb84-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ffb84-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="ffb84-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffb84-141">NOTES</span></span>

## <span data-ttu-id="ffb84-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffb84-142">RELATED LINKS</span></span>
