---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: c59e0f90ae8b6d7839c7bb845b56e31a42b2d033
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412791"
---
# <span data-ttu-id="b2bdf-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="b2bdf-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="b2bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bdf-103">Erstellen eines Benutzerdefinierten Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b2bdf-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b2bdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2bdf-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2bdf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="b2bdf-106">Erstellen eines Benutzerdefinierten Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b2bdf-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b2bdf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="b2bdf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2bdf-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="b2bdf-109">Erstellen eines CustomRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="b2bdf-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="b2bdf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2bdf-110">PARAMETERS</span></span>

### <span data-ttu-id="b2bdf-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="b2bdf-111">-Action</span></span>
<span data-ttu-id="b2bdf-112">Aktionstyp.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-112">Type of Actions.</span></span>
<span data-ttu-id="b2bdf-113">Mögliche Werte sind: "Zulassen", "Blockieren", "Protokoll".</span><span class="sxs-lookup"><span data-stu-id="b2bdf-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="b2bdf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bdf-114">-DefaultProfile</span></span>
<span data-ttu-id="b2bdf-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2bdf-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b2bdf-116">-MatchCondition</span></span>
<span data-ttu-id="b2bdf-117">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-117">List of match conditions.</span></span>

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

### <span data-ttu-id="b2bdf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b2bdf-118">-Name</span></span>
<span data-ttu-id="b2bdf-119">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="b2bdf-119">Name of the rule</span></span>

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

### <span data-ttu-id="b2bdf-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="b2bdf-120">-Priority</span></span>
<span data-ttu-id="b2bdf-121">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="b2bdf-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="b2bdf-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="b2bdf-123">Dauer des Satzlimits.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-123">Rate limit duration.</span></span> <span data-ttu-id="b2bdf-124">Standard – 1 Minute</span><span class="sxs-lookup"><span data-stu-id="b2bdf-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="b2bdf-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="b2bdf-125">-RateLimitThreshold</span></span>
<span data-ttu-id="b2bdf-126">Schwellenwert für Satzbegrenzung</span><span class="sxs-lookup"><span data-stu-id="b2bdf-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="b2bdf-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b2bdf-127">-RuleType</span></span>
<span data-ttu-id="b2bdf-128">Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-128">Type of the rule.</span></span>
<span data-ttu-id="b2bdf-129">Mögliche Werte sind: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="b2bdf-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="b2bdf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bdf-130">CommonParameters</span></span>
<span data-ttu-id="b2bdf-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2bdf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bdf-132">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2bdf-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bdf-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2bdf-133">INPUTS</span></span>

### <span data-ttu-id="b2bdf-134">Keine</span><span class="sxs-lookup"><span data-stu-id="b2bdf-134">None</span></span>

## <span data-ttu-id="b2bdf-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2bdf-135">OUTPUTS</span></span>

### <span data-ttu-id="b2bdf-136">Microsoft.Azure.Commands.FrontDando.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="b2bdf-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="b2bdf-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2bdf-137">NOTES</span></span>

## <span data-ttu-id="b2bdf-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2bdf-138">RELATED LINKS</span></span>

<span data-ttu-id="b2bdf-139">[New-AzFrontDlicWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDlicWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b2bdf-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
