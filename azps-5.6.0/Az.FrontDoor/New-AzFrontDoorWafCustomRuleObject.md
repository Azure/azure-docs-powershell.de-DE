---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: cf74b21d2b07ddf8f92203c43e7005f81cbb2a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928080"
---
# <span data-ttu-id="cc7de-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="cc7de-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="cc7de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc7de-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7de-103">Erstellen von CustomRule-Objekt für die Erstellung von WAF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="cc7de-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="cc7de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc7de-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc7de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc7de-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7de-106">Erstellen von CustomRule-Objekt für die Erstellung von WAF-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="cc7de-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="cc7de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc7de-107">EXAMPLES</span></span>

### <span data-ttu-id="cc7de-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc7de-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="cc7de-109">Erstellen eines CustomRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="cc7de-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="cc7de-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cc7de-110">PARAMETERS</span></span>

### <span data-ttu-id="cc7de-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="cc7de-111">-Action</span></span>
<span data-ttu-id="cc7de-112">Aktionstyp.</span><span class="sxs-lookup"><span data-stu-id="cc7de-112">Type of Actions.</span></span>
<span data-ttu-id="cc7de-113">Mögliche Werte sind: "Zulassen", "Blockieren", "Protokoll"</span><span class="sxs-lookup"><span data-stu-id="cc7de-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="cc7de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7de-114">-DefaultProfile</span></span>
<span data-ttu-id="cc7de-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc7de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc7de-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cc7de-116">-EnabledState</span></span>
<span data-ttu-id="cc7de-117">Aktivierter Zustand.</span><span class="sxs-lookup"><span data-stu-id="cc7de-117">Enabled State.</span></span> <span data-ttu-id="cc7de-118">Mögliche Werte sind: "Aktiviert", "Deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="cc7de-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="cc7de-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="cc7de-119">-MatchCondition</span></span>
<span data-ttu-id="cc7de-120">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="cc7de-120">List of match conditions.</span></span>

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

### <span data-ttu-id="cc7de-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc7de-121">-Name</span></span>
<span data-ttu-id="cc7de-122">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="cc7de-122">Name of the rule</span></span>

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

### <span data-ttu-id="cc7de-123">-Priorität</span><span class="sxs-lookup"><span data-stu-id="cc7de-123">-Priority</span></span>
<span data-ttu-id="cc7de-124">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="cc7de-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="cc7de-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="cc7de-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="cc7de-126">Zinslimitdauer.</span><span class="sxs-lookup"><span data-stu-id="cc7de-126">Rate limit duration.</span></span> <span data-ttu-id="cc7de-127">Standard : 1 Minute</span><span class="sxs-lookup"><span data-stu-id="cc7de-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="cc7de-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="cc7de-128">-RateLimitThreshold</span></span>
<span data-ttu-id="cc7de-129">Schwellenwert für Die Zinsgrenze</span><span class="sxs-lookup"><span data-stu-id="cc7de-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="cc7de-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="cc7de-130">-RuleType</span></span>
<span data-ttu-id="cc7de-131">Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="cc7de-131">Type of the rule.</span></span>
<span data-ttu-id="cc7de-132">Mögliche Werte sind: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="cc7de-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="cc7de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7de-133">CommonParameters</span></span>
<span data-ttu-id="cc7de-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc7de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7de-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc7de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7de-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc7de-136">INPUTS</span></span>

### <span data-ttu-id="cc7de-137">Keine</span><span class="sxs-lookup"><span data-stu-id="cc7de-137">None</span></span>

## <span data-ttu-id="cc7de-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc7de-138">OUTPUTS</span></span>

### <span data-ttu-id="cc7de-139">Microsoft.Azure.Commands.Frontdoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="cc7de-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="cc7de-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cc7de-140">NOTES</span></span>

## <span data-ttu-id="cc7de-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cc7de-141">RELATED LINKS</span></span>

<span data-ttu-id="cc7de-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="cc7de-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
