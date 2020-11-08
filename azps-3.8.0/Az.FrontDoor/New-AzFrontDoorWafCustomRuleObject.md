---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: d352f70d28b9bfafae46697fb6d69dc50c739b19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004044"
---
# <span data-ttu-id="cfb24-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="cfb24-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="cfb24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfb24-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb24-103">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="cfb24-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="cfb24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb24-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfb24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfb24-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb24-106">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="cfb24-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="cfb24-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfb24-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb24-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfb24-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="cfb24-109">Erstellen eines CustomRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="cfb24-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="cfb24-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb24-110">PARAMETERS</span></span>

### <span data-ttu-id="cfb24-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="cfb24-111">-Action</span></span>
<span data-ttu-id="cfb24-112">Art der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="cfb24-112">Type of Actions.</span></span>
<span data-ttu-id="cfb24-113">Mögliche Werte sind: ' allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="cfb24-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="cfb24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb24-114">-DefaultProfile</span></span>
<span data-ttu-id="cfb24-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfb24-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb24-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cfb24-116">-EnabledState</span></span>
<span data-ttu-id="cfb24-117">Status aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cfb24-117">Enabled State.</span></span> <span data-ttu-id="cfb24-118">Mögliche Werte sind: "aktiviert", "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="cfb24-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="cfb24-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="cfb24-119">-MatchCondition</span></span>
<span data-ttu-id="cfb24-120">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="cfb24-120">List of match conditions.</span></span>

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

### <span data-ttu-id="cfb24-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cfb24-121">-Name</span></span>
<span data-ttu-id="cfb24-122">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="cfb24-122">Name of the rule</span></span>

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

### <span data-ttu-id="cfb24-123">-Priorität</span><span class="sxs-lookup"><span data-stu-id="cfb24-123">-Priority</span></span>
<span data-ttu-id="cfb24-124">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="cfb24-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="cfb24-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="cfb24-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="cfb24-126">Kurs Beschränkungs Dauer.</span><span class="sxs-lookup"><span data-stu-id="cfb24-126">Rate limit duration.</span></span> <span data-ttu-id="cfb24-127">Standard-1 Minute</span><span class="sxs-lookup"><span data-stu-id="cfb24-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="cfb24-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="cfb24-128">-RateLimitThreshold</span></span>
<span data-ttu-id="cfb24-129">Schwellenwert für die Gebührenobergrenze</span><span class="sxs-lookup"><span data-stu-id="cfb24-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="cfb24-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="cfb24-130">-RuleType</span></span>
<span data-ttu-id="cfb24-131">Der Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="cfb24-131">Type of the rule.</span></span>
<span data-ttu-id="cfb24-132">Mögliche Werte sind: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="cfb24-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="cfb24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb24-133">CommonParameters</span></span>
<span data-ttu-id="cfb24-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb24-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfb24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb24-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfb24-136">INPUTS</span></span>

### <span data-ttu-id="cfb24-137">Keine</span><span class="sxs-lookup"><span data-stu-id="cfb24-137">None</span></span>

## <span data-ttu-id="cfb24-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfb24-138">OUTPUTS</span></span>

### <span data-ttu-id="cfb24-139">Microsoft. Azure. Commands. Haustür. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="cfb24-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="cfb24-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfb24-140">NOTES</span></span>

## <span data-ttu-id="cfb24-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfb24-141">RELATED LINKS</span></span>

<span data-ttu-id="cfb24-142">[Neu – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Satz-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="cfb24-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
