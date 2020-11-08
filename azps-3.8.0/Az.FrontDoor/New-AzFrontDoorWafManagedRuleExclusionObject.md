---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 319f2779986f71f4396b1b28815784bc4cd05def
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004046"
---
# <span data-ttu-id="bba43-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="bba43-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="bba43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bba43-102">SYNOPSIS</span></span>
<span data-ttu-id="bba43-103">Erstellen Sie ein Ausschluss Objekt für verwaltete Regel für WAF-verwaltete Regelsätze, Gruppen oder Regeln.</span><span class="sxs-lookup"><span data-stu-id="bba43-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="bba43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba43-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba43-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bba43-105">DESCRIPTION</span></span>
<span data-ttu-id="bba43-106">Erstellen Sie ein Ausschluss Objekt für verwaltete Regel für WAF-verwaltete Regelsätze, Gruppen oder Regeln.</span><span class="sxs-lookup"><span data-stu-id="bba43-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="bba43-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bba43-107">EXAMPLES</span></span>

### <span data-ttu-id="bba43-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bba43-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="bba43-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bba43-109">PARAMETERS</span></span>

### <span data-ttu-id="bba43-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba43-110">-DefaultProfile</span></span>
<span data-ttu-id="bba43-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bba43-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba43-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="bba43-112">-Operator</span></span>
<span data-ttu-id="bba43-113">Der Operator, der beim Abgleich mit der Auswahl verwendet werden soll, EqualsAny bedeutet keine Auswahl (alle mit Variablen des angegebenen Typs übereinstimmen).</span><span class="sxs-lookup"><span data-stu-id="bba43-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba43-114">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="bba43-114">-Selector</span></span>
<span data-ttu-id="bba43-115">Auswahlmuster, das mit dem Operator übereinstimmen soll (wenn der Operator nicht EqualsAny ist)</span><span class="sxs-lookup"><span data-stu-id="bba43-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba43-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="bba43-116">-Variable</span></span>
<span data-ttu-id="bba43-117">Variable vergleichen.</span><span class="sxs-lookup"><span data-stu-id="bba43-117">Match variable.</span></span> <span data-ttu-id="bba43-118">Mögliche Werte sind RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="bba43-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="bba43-119">Beispielsweise ist QueryStringArgNames ein Ausschluss von Get-Parametern, die dem Selektor mit dem angegebenen Operator entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bba43-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba43-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba43-120">CommonParameters</span></span>
<span data-ttu-id="bba43-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba43-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba43-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bba43-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba43-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bba43-123">INPUTS</span></span>

### <span data-ttu-id="bba43-124">Keine</span><span class="sxs-lookup"><span data-stu-id="bba43-124">None</span></span>

## <span data-ttu-id="bba43-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bba43-125">OUTPUTS</span></span>

### <span data-ttu-id="bba43-126">Microsoft. Azure. Commands. Haustür. Models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="bba43-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="bba43-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="bba43-127">NOTES</span></span>

## <span data-ttu-id="bba43-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bba43-128">RELATED LINKS</span></span>
<span data-ttu-id="bba43-129">[Neu – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Neu – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [Neu – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="bba43-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
