---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152164"
---
# <span data-ttu-id="bf543-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bf543-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bf543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf543-102">SYNOPSIS</span></span>
<span data-ttu-id="bf543-103">Erstellt ein Objekt vom Typ "Warnungsaktion"</span><span class="sxs-lookup"><span data-stu-id="bf543-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="bf543-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf543-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf543-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf543-105">DESCRIPTION</span></span>
<span data-ttu-id="bf543-106">Erstellt ein Objekt vom Typ "Warnungsaktion". Dieses Objekt soll an den Befehl übergeben werden, mit dem eine Protokollwarnungsregel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf543-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="bf543-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf543-107">EXAMPLES</span></span>

### <span data-ttu-id="bf543-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf543-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="bf543-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf543-109">PARAMETERS</span></span>

### <span data-ttu-id="bf543-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="bf543-110">-AznsAction</span></span>
<span data-ttu-id="bf543-111">Die Details der AzNS-Aktion</span><span class="sxs-lookup"><span data-stu-id="bf543-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf543-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf543-112">-DefaultProfile</span></span>
<span data-ttu-id="bf543-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf543-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf543-114">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="bf543-114">-Severity</span></span>
<span data-ttu-id="bf543-115">Der Schweregrad für diese Warnung</span><span class="sxs-lookup"><span data-stu-id="bf543-115">The severity for this alert</span></span>

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

### <span data-ttu-id="bf543-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="bf543-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="bf543-117">Die Dauer in Minuten, für die eine Warnung gedrosselt werden soll</span><span class="sxs-lookup"><span data-stu-id="bf543-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf543-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="bf543-118">-Trigger</span></span>
<span data-ttu-id="bf543-119">Warnungsauslöserbedingung</span><span class="sxs-lookup"><span data-stu-id="bf543-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf543-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf543-120">CommonParameters</span></span>
<span data-ttu-id="bf543-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf543-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf543-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf543-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf543-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf543-123">INPUTS</span></span>

### <span data-ttu-id="bf543-124">Keine</span><span class="sxs-lookup"><span data-stu-id="bf543-124">None</span></span>

## <span data-ttu-id="bf543-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf543-125">OUTPUTS</span></span>

### <span data-ttu-id="bf543-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bf543-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bf543-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf543-127">NOTES</span></span>

## <span data-ttu-id="bf543-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf543-128">RELATED LINKS</span></span>
