---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180250"
---
# <span data-ttu-id="7e076-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7e076-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="7e076-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e076-102">SYNOPSIS</span></span>
<span data-ttu-id="7e076-103">Ruft geplante Abfrage Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="7e076-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="7e076-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e076-104">SYNTAX</span></span>

### <span data-ttu-id="7e076-105">BySubscriptionOrResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e076-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e076-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="7e076-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e076-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e076-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e076-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e076-108">DESCRIPTION</span></span>
<span data-ttu-id="7e076-109">Ruft geplante Abfrage Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="7e076-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="7e076-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e076-110">EXAMPLES</span></span>

### <span data-ttu-id="7e076-111">Beispiel 1: Liste nach Abonnement oder Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7e076-111">Example 1: List by subscription or resource group</span></span>
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

### <span data-ttu-id="7e076-112">Beispiel 2: Abrufen nach Regelnamen</span><span class="sxs-lookup"><span data-stu-id="7e076-112">Example 2: Get by rule name</span></span>
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

### <span data-ttu-id="7e076-113">Beispiel 3: Abrufen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7e076-113">Example 3: Get by resource Id</span></span>
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

## <span data-ttu-id="7e076-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e076-114">PARAMETERS</span></span>

### <span data-ttu-id="7e076-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e076-115">-DefaultProfile</span></span>
<span data-ttu-id="7e076-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e076-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e076-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7e076-117">-Name</span></span>
<span data-ttu-id="7e076-118">Der Name der Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="7e076-118">The alert rule name</span></span>

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

### <span data-ttu-id="7e076-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e076-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e076-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7e076-120">The resource group name</span></span>

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

### <span data-ttu-id="7e076-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7e076-121">-ResourceId</span></span>
<span data-ttu-id="7e076-122">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7e076-122">The resource Id</span></span>

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

### <span data-ttu-id="7e076-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e076-123">CommonParameters</span></span>
<span data-ttu-id="7e076-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e076-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e076-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e076-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e076-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e076-126">INPUTS</span></span>

### <span data-ttu-id="7e076-127">Keine</span><span class="sxs-lookup"><span data-stu-id="7e076-127">None</span></span>

## <span data-ttu-id="7e076-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e076-128">OUTPUTS</span></span>

### <span data-ttu-id="7e076-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="7e076-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="7e076-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e076-130">NOTES</span></span>

## <span data-ttu-id="7e076-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e076-131">RELATED LINKS</span></span>
