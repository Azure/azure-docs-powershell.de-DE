---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174728"
---
# <span data-ttu-id="a81ad-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="a81ad-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="a81ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a81ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a81ad-103">Erstellen Sie ein Ausschluss Objekt für verwaltete Regel für WAF-verwaltete Regelsätze, Gruppen oder Regeln.</span><span class="sxs-lookup"><span data-stu-id="a81ad-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="a81ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a81ad-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a81ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a81ad-105">DESCRIPTION</span></span>
<span data-ttu-id="a81ad-106">Erstellen Sie ein Ausschluss Objekt für verwaltete Regel für WAF-verwaltete Regelsätze, Gruppen oder Regeln.</span><span class="sxs-lookup"><span data-stu-id="a81ad-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="a81ad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a81ad-107">EXAMPLES</span></span>

### <span data-ttu-id="a81ad-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a81ad-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="a81ad-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a81ad-109">PARAMETERS</span></span>

### <span data-ttu-id="a81ad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81ad-110">-DefaultProfile</span></span>
<span data-ttu-id="a81ad-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a81ad-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a81ad-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="a81ad-112">-Operator</span></span>
<span data-ttu-id="a81ad-113">Der Operator, der beim Abgleich mit der Auswahl verwendet werden soll, EqualsAny bedeutet keine Auswahl (alle mit Variablen des angegebenen Typs übereinstimmen).</span><span class="sxs-lookup"><span data-stu-id="a81ad-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="a81ad-114">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="a81ad-114">-Selector</span></span>
<span data-ttu-id="a81ad-115">Auswahlmuster, das mit dem Operator übereinstimmen soll (wenn der Operator nicht EqualsAny ist)</span><span class="sxs-lookup"><span data-stu-id="a81ad-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="a81ad-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="a81ad-116">-Variable</span></span>
<span data-ttu-id="a81ad-117">Variable vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a81ad-117">Match variable.</span></span> <span data-ttu-id="a81ad-118">Mögliche Werte sind RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="a81ad-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="a81ad-119">Beispielsweise ist QueryStringArgNames ein Ausschluss von Get-Parametern, die dem Selektor mit dem angegebenen Operator entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a81ad-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="a81ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81ad-120">CommonParameters</span></span>
<span data-ttu-id="a81ad-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a81ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81ad-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a81ad-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81ad-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a81ad-123">INPUTS</span></span>

### <span data-ttu-id="a81ad-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a81ad-124">None</span></span>

## <span data-ttu-id="a81ad-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a81ad-125">OUTPUTS</span></span>

### <span data-ttu-id="a81ad-126">Microsoft. Azure. Commands. Haustür. Models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="a81ad-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="a81ad-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a81ad-127">NOTES</span></span>

## <span data-ttu-id="a81ad-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a81ad-128">RELATED LINKS</span></span>

<span data-ttu-id="a81ad-129">[Neu – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Neu – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [Neu – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="a81ad-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
