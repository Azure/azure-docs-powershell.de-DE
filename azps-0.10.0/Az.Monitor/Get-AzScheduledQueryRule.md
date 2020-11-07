---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 1cb05a83ccbe1786392867f4714553413fe635c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842015"
---
# <span data-ttu-id="f7423-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7423-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f7423-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7423-102">SYNOPSIS</span></span>
<span data-ttu-id="f7423-103">Ruft geplante Abfrage Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="f7423-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="f7423-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7423-104">SYNTAX</span></span>

### <span data-ttu-id="f7423-105">BySubscriptionOrResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7423-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7423-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="f7423-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7423-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7423-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7423-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7423-108">DESCRIPTION</span></span>
<span data-ttu-id="f7423-109">Ruft geplante Abfrage Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="f7423-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="f7423-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7423-110">EXAMPLES</span></span>

### <span data-ttu-id="f7423-111">Beispiel 1 – Liste nach Abonnement oder Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f7423-111">Example 1 - List by subscription or resource group</span></span>
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

### <span data-ttu-id="f7423-112">Beispiel 2: Abrufen des Regel namens</span><span class="sxs-lookup"><span data-stu-id="f7423-112">Example 2 - Get by rule name</span></span>
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

### <span data-ttu-id="f7423-113">Beispiel 3: Abrufen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f7423-113">Example 3 - Get by resource Id</span></span>
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

## <span data-ttu-id="f7423-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7423-114">PARAMETERS</span></span>

### <span data-ttu-id="f7423-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7423-115">-DefaultProfile</span></span>
<span data-ttu-id="f7423-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7423-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7423-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f7423-117">-Name</span></span>
<span data-ttu-id="f7423-118">Der Name der Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="f7423-118">The alert rule name</span></span>

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

### <span data-ttu-id="f7423-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7423-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7423-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f7423-120">The resource group name</span></span>

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

### <span data-ttu-id="f7423-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f7423-121">-ResourceId</span></span>
<span data-ttu-id="f7423-122">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f7423-122">The resource Id</span></span>

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

### <span data-ttu-id="f7423-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7423-123">CommonParameters</span></span>
<span data-ttu-id="f7423-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7423-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7423-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7423-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7423-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7423-126">INPUTS</span></span>

### <span data-ttu-id="f7423-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f7423-127">None</span></span>

## <span data-ttu-id="f7423-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7423-128">OUTPUTS</span></span>

### <span data-ttu-id="f7423-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f7423-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f7423-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7423-130">NOTES</span></span>

## <span data-ttu-id="f7423-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7423-131">RELATED LINKS</span></span>
