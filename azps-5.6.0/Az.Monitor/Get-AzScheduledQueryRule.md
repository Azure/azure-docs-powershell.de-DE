---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 98590e23035810317bf4290513a1c0030b0fcac0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932579"
---
# <span data-ttu-id="3f2b4-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f2b4-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="3f2b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2b4-103">Ruft geplante Abfrageressourcen ab</span><span class="sxs-lookup"><span data-stu-id="3f2b4-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="3f2b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f2b4-104">SYNTAX</span></span>

### <span data-ttu-id="3f2b4-105">BySubscriptionOrResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f2b4-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2b4-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="3f2b4-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2b4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2b4-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f2b4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f2b4-108">DESCRIPTION</span></span>
<span data-ttu-id="3f2b4-109">Ruft geplante Abfrageressourcen ab</span><span class="sxs-lookup"><span data-stu-id="3f2b4-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="3f2b4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f2b4-110">EXAMPLES</span></span>

### <span data-ttu-id="3f2b4-111">Beispiel 1: Liste nach Abonnement oder Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3f2b4-111">Example 1: List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="3f2b4-112">Beispiel 2: Nach Regelname erhalten</span><span class="sxs-lookup"><span data-stu-id="3f2b4-112">Example 2: Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

### <span data-ttu-id="3f2b4-113">Beispiel 3: Nach Ressourcen-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="3f2b4-113">Example 3: Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

## <span data-ttu-id="3f2b4-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f2b4-114">PARAMETERS</span></span>

### <span data-ttu-id="3f2b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2b4-115">-DefaultProfile</span></span>
<span data-ttu-id="3f2b4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2b4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3f2b4-117">-Name</span></span>
<span data-ttu-id="3f2b4-118">Der Name der Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="3f2b4-118">The alert rule name</span></span>

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

### <span data-ttu-id="3f2b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f2b4-120">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3f2b4-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="3f2b4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2b4-121">-ResourceId</span></span>
<span data-ttu-id="3f2b4-122">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3f2b4-122">The resource Id</span></span>

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

### <span data-ttu-id="3f2b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2b4-123">CommonParameters</span></span>
<span data-ttu-id="3f2b4-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2b4-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f2b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2b4-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f2b4-126">INPUTS</span></span>

### <span data-ttu-id="3f2b4-127">Keine</span><span class="sxs-lookup"><span data-stu-id="3f2b4-127">None</span></span>

## <span data-ttu-id="3f2b4-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f2b4-128">OUTPUTS</span></span>

### <span data-ttu-id="3f2b4-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3f2b4-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="3f2b4-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f2b4-130">NOTES</span></span>

## <span data-ttu-id="3f2b4-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f2b4-131">RELATED LINKS</span></span>
