---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820055"
---
# <span data-ttu-id="c6344-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6344-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="c6344-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6344-102">SYNOPSIS</span></span>
<span data-ttu-id="c6344-103">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="c6344-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c6344-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6344-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6344-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6344-105">DESCRIPTION</span></span>
<span data-ttu-id="c6344-106">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="c6344-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c6344-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6344-107">EXAMPLES</span></span>

### <span data-ttu-id="c6344-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6344-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="c6344-109">Erstellen eines CustomRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="c6344-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="c6344-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6344-110">PARAMETERS</span></span>

### <span data-ttu-id="c6344-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="c6344-111">-Action</span></span>
<span data-ttu-id="c6344-112">Art der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="c6344-112">Type of Actions.</span></span>
<span data-ttu-id="c6344-113">Mögliche Werte sind: ' allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="c6344-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6344-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6344-114">-DefaultProfile</span></span>
<span data-ttu-id="c6344-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6344-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6344-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="c6344-116">-MatchCondition</span></span>
<span data-ttu-id="c6344-117">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="c6344-117">List of match conditions.</span></span>

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

### <span data-ttu-id="c6344-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c6344-118">-Name</span></span>
<span data-ttu-id="c6344-119">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="c6344-119">Name of the rule</span></span>

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

### <span data-ttu-id="c6344-120">-Priorität</span><span class="sxs-lookup"><span data-stu-id="c6344-120">-Priority</span></span>
<span data-ttu-id="c6344-121">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="c6344-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="c6344-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="c6344-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="c6344-123">Kurs Beschränkungs Dauer.</span><span class="sxs-lookup"><span data-stu-id="c6344-123">Rate limit duration.</span></span> <span data-ttu-id="c6344-124">Standard-1 Minute</span><span class="sxs-lookup"><span data-stu-id="c6344-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="c6344-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="c6344-125">-RateLimitThreshold</span></span>
<span data-ttu-id="c6344-126">Rate Limit keine</span><span class="sxs-lookup"><span data-stu-id="c6344-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="c6344-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c6344-127">-RuleType</span></span>
<span data-ttu-id="c6344-128">Der Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="c6344-128">Type of the rule.</span></span>
<span data-ttu-id="c6344-129">Mögliche Werte sind: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="c6344-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6344-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6344-130">CommonParameters</span></span>
<span data-ttu-id="c6344-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6344-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6344-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6344-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6344-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6344-133">INPUTS</span></span>

### <span data-ttu-id="c6344-134">Keine</span><span class="sxs-lookup"><span data-stu-id="c6344-134">None</span></span>

## <span data-ttu-id="c6344-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6344-135">OUTPUTS</span></span>

### <span data-ttu-id="c6344-136">Microsoft. Azure. Commands. Haustür. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="c6344-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="c6344-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6344-137">NOTES</span></span>

## <span data-ttu-id="c6344-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6344-138">RELATED LINKS</span></span>

<span data-ttu-id="c6344-139">[Neu – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Satz-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c6344-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
