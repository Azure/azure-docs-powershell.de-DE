---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306288"
---
# <span data-ttu-id="a3e3a-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="a3e3a-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="a3e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e3a-103">Erstellen eines Benutzerdefinierten Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a3e3a-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="a3e3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3e3a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e3a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e3a-106">Erstellen eines Benutzerdefinierten Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a3e3a-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="a3e3a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="a3e3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3e3a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="a3e3a-109">Erstellen eines Benutzerdefinierten Objekts</span><span class="sxs-lookup"><span data-stu-id="a3e3a-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="a3e3a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3e3a-110">PARAMETERS</span></span>

### <span data-ttu-id="a3e3a-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="a3e3a-111">-Action</span></span>
<span data-ttu-id="a3e3a-112">Aktionstyp.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-112">Type of Actions.</span></span>
<span data-ttu-id="a3e3a-113">Mögliche Werte sind: "Zulassen", "Blockieren", "Protokoll".</span><span class="sxs-lookup"><span data-stu-id="a3e3a-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="a3e3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e3a-114">-DefaultProfile</span></span>
<span data-ttu-id="a3e3a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3e3a-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="a3e3a-116">-EnabledState</span></span>
<span data-ttu-id="a3e3a-117">Status "Enabled".</span><span class="sxs-lookup"><span data-stu-id="a3e3a-117">Enabled State.</span></span> <span data-ttu-id="a3e3a-118">Mögliche Werte sind: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="a3e3a-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e3a-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="a3e3a-119">-MatchCondition</span></span>
<span data-ttu-id="a3e3a-120">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-120">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e3a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3e3a-121">-Name</span></span>
<span data-ttu-id="a3e3a-122">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="a3e3a-122">Name of the rule</span></span>

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

### <span data-ttu-id="a3e3a-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="a3e3a-123">-Priority</span></span>
<span data-ttu-id="a3e3a-124">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="a3e3a-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="a3e3a-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="a3e3a-126">Dauer des Satzlimits.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-126">Rate limit duration.</span></span> <span data-ttu-id="a3e3a-127">Standard – 1 Minute</span><span class="sxs-lookup"><span data-stu-id="a3e3a-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="a3e3a-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="a3e3a-128">-RateLimitThreshold</span></span>
<span data-ttu-id="a3e3a-129">Schwellenwert für satzbegrenzung</span><span class="sxs-lookup"><span data-stu-id="a3e3a-129">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e3a-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="a3e3a-130">-RuleType</span></span>
<span data-ttu-id="a3e3a-131">Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-131">Type of the rule.</span></span>
<span data-ttu-id="a3e3a-132">Mögliche Werte sind: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="a3e3a-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="a3e3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e3a-133">CommonParameters</span></span>
<span data-ttu-id="a3e3a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e3a-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3e3a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e3a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3e3a-136">INPUTS</span></span>

### <span data-ttu-id="a3e3a-137">Keine</span><span class="sxs-lookup"><span data-stu-id="a3e3a-137">None</span></span>

## <span data-ttu-id="a3e3a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3e3a-138">OUTPUTS</span></span>

### <span data-ttu-id="a3e3a-139">Microsoft.Azure.Commands.FrontDando.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="a3e3a-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="a3e3a-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3e3a-140">NOTES</span></span>

## <span data-ttu-id="a3e3a-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3e3a-141">RELATED LINKS</span></span>

<span data-ttu-id="a3e3a-142">[New-AzFrontDlicWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDlicWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a3e3a-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
