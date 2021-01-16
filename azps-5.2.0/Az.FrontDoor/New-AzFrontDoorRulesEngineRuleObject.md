---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292144"
---
# <span data-ttu-id="bac0c-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="bac0c-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="bac0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac0c-102">SYNOPSIS</span></span>
<span data-ttu-id="bac0c-103">Erstellen Sie ein "PSRulesEngineRule"-Objekt für die Erstellung von Regeln der Engine.</span><span class="sxs-lookup"><span data-stu-id="bac0c-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="bac0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bac0c-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bac0c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bac0c-105">DESCRIPTION</span></span>
<span data-ttu-id="bac0c-106">Erstellen Sie ein "PSRulesEngineRule"-Objekt für die Erstellung von Regeln der Engine.</span><span class="sxs-lookup"><span data-stu-id="bac0c-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="bac0c-107">Verwenden Sie das Cmdlet "New-AzFrontDtunRulesEngineActionObject", um ein PSRulesEngineAction-Objekt zum Übergeben an den Parameter "-Action" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bac0c-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="bac0c-108">Verwenden Sie das Cmdlet "New-AzFrontDmatchRulesEngineMatchConditionObject", um ein PSRulesEngineMatchCondition-Objekt zu erstellen, das an den Parameter "-MatchCondition" übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bac0c-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="bac0c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bac0c-109">EXAMPLES</span></span>

### <span data-ttu-id="bac0c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bac0c-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="bac0c-111">Erstellen Sie ein neues PSRulesEngineRule-Objekt, und zeigen Sie, wie die Unterfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bac0c-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="bac0c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bac0c-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="bac0c-113">Beim Übergeben eines ungültigen Prioritätswerts wird eine Ausgabe erwartet.</span><span class="sxs-lookup"><span data-stu-id="bac0c-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="bac0c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bac0c-114">PARAMETERS</span></span>

### <span data-ttu-id="bac0c-115">-Aktion</span><span class="sxs-lookup"><span data-stu-id="bac0c-115">-Action</span></span>
<span data-ttu-id="bac0c-116">Aktionen, die für die Anforderung und Antwort durchzuführen sind, wenn alle Übereinstimmungsbedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="bac0c-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac0c-117">-DefaultProfile</span></span>
<span data-ttu-id="bac0c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bac0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bac0c-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="bac0c-119">-MatchCondition</span></span>
<span data-ttu-id="bac0c-120">Eine Liste der Übereinstimmungsbedingungen, die erfüllt sein müssen, damit die Aktionen dieser Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bac0c-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="bac0c-121">Wenn keine Übereinstimmungsbedingungen gelten, werden die Aktionen immer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bac0c-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac0c-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="bac0c-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="bac0c-123">Wenn diese Regel eine Übereinstimmung ist, sollte das Regelmodul weiterhin die verbleibenden Regeln ausführen oder beenden.</span><span class="sxs-lookup"><span data-stu-id="bac0c-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="bac0c-124">Mögliche Werte sind "Continue" und "Stop".</span><span class="sxs-lookup"><span data-stu-id="bac0c-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="bac0c-125">Ist dies nicht der Fall, wird standardmäßig "Weiter" verwendet.</span><span class="sxs-lookup"><span data-stu-id="bac0c-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac0c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bac0c-126">-Name</span></span>
<span data-ttu-id="bac0c-127">Ein Name, der auf diese bestimmte Regel bezugt.</span><span class="sxs-lookup"><span data-stu-id="bac0c-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="bac0c-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="bac0c-128">-Priority</span></span>
<span data-ttu-id="bac0c-129">Eine dieser Regel zugewiesene Priorität.</span><span class="sxs-lookup"><span data-stu-id="bac0c-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="bac0c-130">Kann nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="bac0c-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac0c-131">CommonParameters</span></span>
<span data-ttu-id="bac0c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac0c-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bac0c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac0c-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bac0c-134">INPUTS</span></span>

### <span data-ttu-id="bac0c-135">Keine</span><span class="sxs-lookup"><span data-stu-id="bac0c-135">None</span></span>

## <span data-ttu-id="bac0c-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bac0c-136">OUTPUTS</span></span>

### <span data-ttu-id="bac0c-137">Microsoft.Azure.Commands.Frontd selbst.Models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="bac0c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="bac0c-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bac0c-138">NOTES</span></span>

## <span data-ttu-id="bac0c-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bac0c-139">RELATED LINKS</span></span>
