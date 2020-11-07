---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651118"
---
# <span data-ttu-id="64ce7-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="64ce7-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="64ce7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="64ce7-103">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="64ce7-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="64ce7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64ce7-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ce7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="64ce7-106">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="64ce7-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="64ce7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="64ce7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64ce7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="64ce7-109">Erstellen eines CustomRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="64ce7-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="64ce7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64ce7-110">PARAMETERS</span></span>

### <span data-ttu-id="64ce7-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="64ce7-111">-Action</span></span>
<span data-ttu-id="64ce7-112">Art der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="64ce7-112">Type of Actions.</span></span>
<span data-ttu-id="64ce7-113">Mögliche Werte sind: ' allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="64ce7-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="64ce7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ce7-114">-DefaultProfile</span></span>
<span data-ttu-id="64ce7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64ce7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ce7-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="64ce7-116">-MatchCondition</span></span>
<span data-ttu-id="64ce7-117">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="64ce7-117">List of match conditions.</span></span>

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

### <span data-ttu-id="64ce7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="64ce7-118">-Name</span></span>
<span data-ttu-id="64ce7-119">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="64ce7-119">Name of the rule</span></span>

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

### <span data-ttu-id="64ce7-120">-Priorität</span><span class="sxs-lookup"><span data-stu-id="64ce7-120">-Priority</span></span>
<span data-ttu-id="64ce7-121">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="64ce7-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="64ce7-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="64ce7-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="64ce7-123">Kurs Beschränkungs Dauer.</span><span class="sxs-lookup"><span data-stu-id="64ce7-123">Rate limit duration.</span></span> <span data-ttu-id="64ce7-124">Standard-1 Minute</span><span class="sxs-lookup"><span data-stu-id="64ce7-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="64ce7-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="64ce7-125">-RateLimitThreshold</span></span>
<span data-ttu-id="64ce7-126">Schwellenwert für die Gebührenobergrenze</span><span class="sxs-lookup"><span data-stu-id="64ce7-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="64ce7-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="64ce7-127">-RuleType</span></span>
<span data-ttu-id="64ce7-128">Der Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="64ce7-128">Type of the rule.</span></span>
<span data-ttu-id="64ce7-129">Mögliche Werte sind: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="64ce7-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="64ce7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ce7-130">CommonParameters</span></span>
<span data-ttu-id="64ce7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ce7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ce7-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64ce7-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ce7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64ce7-133">INPUTS</span></span>

### <span data-ttu-id="64ce7-134">Keine</span><span class="sxs-lookup"><span data-stu-id="64ce7-134">None</span></span>

## <span data-ttu-id="64ce7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64ce7-135">OUTPUTS</span></span>

### <span data-ttu-id="64ce7-136">Microsoft. Azure. Commands. Haustür. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="64ce7-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="64ce7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="64ce7-137">NOTES</span></span>

## <span data-ttu-id="64ce7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64ce7-138">RELATED LINKS</span></span>

<span data-ttu-id="64ce7-139">[Neu – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Satz-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="64ce7-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
