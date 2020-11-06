---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476065"
---
# <span data-ttu-id="f286c-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="f286c-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="f286c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f286c-102">SYNOPSIS</span></span>
<span data-ttu-id="f286c-103">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="f286c-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f286c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f286c-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f286c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f286c-105">DESCRIPTION</span></span>
<span data-ttu-id="f286c-106">Erstellen eines CustomRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="f286c-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f286c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f286c-107">EXAMPLES</span></span>

### <span data-ttu-id="f286c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f286c-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="f286c-109">Erstellen eines CustomRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="f286c-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="f286c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f286c-110">PARAMETERS</span></span>

### <span data-ttu-id="f286c-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="f286c-111">-Action</span></span>
<span data-ttu-id="f286c-112">Art der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f286c-112">Type of Actions.</span></span>
<span data-ttu-id="f286c-113">Mögliche Werte sind: ' allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="f286c-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f286c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f286c-114">-DefaultProfile</span></span>
<span data-ttu-id="f286c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f286c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f286c-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="f286c-116">-MatchCondition</span></span>
<span data-ttu-id="f286c-117">Liste der Übereinstimmungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="f286c-117">List of match conditions.</span></span>

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

### <span data-ttu-id="f286c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f286c-118">-Name</span></span>
<span data-ttu-id="f286c-119">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="f286c-119">Name of the rule</span></span>

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

### <span data-ttu-id="f286c-120">-Priorität</span><span class="sxs-lookup"><span data-stu-id="f286c-120">-Priority</span></span>
<span data-ttu-id="f286c-121">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="f286c-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="f286c-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="f286c-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="f286c-123">Kurs Beschränkungs Dauer.</span><span class="sxs-lookup"><span data-stu-id="f286c-123">Rate limit duration.</span></span> <span data-ttu-id="f286c-124">Standard-1 Minute</span><span class="sxs-lookup"><span data-stu-id="f286c-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="f286c-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="f286c-125">-RateLimitThreshold</span></span>
<span data-ttu-id="f286c-126">Rate Limit keine</span><span class="sxs-lookup"><span data-stu-id="f286c-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="f286c-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f286c-127">-RuleType</span></span>
<span data-ttu-id="f286c-128">Der Typ der Regel.</span><span class="sxs-lookup"><span data-stu-id="f286c-128">Type of the rule.</span></span>
<span data-ttu-id="f286c-129">Mögliche Werte sind: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="f286c-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="f286c-130">-Transform</span><span class="sxs-lookup"><span data-stu-id="f286c-130">-Transform</span></span>
<span data-ttu-id="f286c-131">Liste der Transformationen</span><span class="sxs-lookup"><span data-stu-id="f286c-131">List of transforms</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f286c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f286c-132">CommonParameters</span></span>
<span data-ttu-id="f286c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f286c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f286c-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f286c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f286c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f286c-135">INPUTS</span></span>

### <span data-ttu-id="f286c-136">Keine</span><span class="sxs-lookup"><span data-stu-id="f286c-136">None</span></span>

## <span data-ttu-id="f286c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f286c-137">OUTPUTS</span></span>

### <span data-ttu-id="f286c-138">Microsoft. Azure. Commands. Haustür. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="f286c-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="f286c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f286c-139">NOTES</span></span>

## <span data-ttu-id="f286c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f286c-140">RELATED LINKS</span></span>

<span data-ttu-id="f286c-141">[Neu – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Satz-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f286c-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
