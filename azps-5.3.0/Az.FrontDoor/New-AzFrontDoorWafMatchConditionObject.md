---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469771"
---
# <span data-ttu-id="09684-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="09684-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="09684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09684-102">SYNOPSIS</span></span>
<span data-ttu-id="09684-103">Erstellen eines "MatchCondition"-Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="09684-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="09684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09684-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09684-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09684-105">DESCRIPTION</span></span>
<span data-ttu-id="09684-106">Erstellen eines "MatchCondition"-Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="09684-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="09684-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09684-107">EXAMPLES</span></span>

### <span data-ttu-id="09684-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09684-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="09684-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="09684-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="09684-110">Erstellen eines "MatchCondition"-Objekts</span><span class="sxs-lookup"><span data-stu-id="09684-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="09684-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09684-111">PARAMETERS</span></span>

### <span data-ttu-id="09684-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09684-112">-DefaultProfile</span></span>
<span data-ttu-id="09684-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09684-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09684-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="09684-114">-MatchValue</span></span>
<span data-ttu-id="09684-115">Übereinstimmungswert.</span><span class="sxs-lookup"><span data-stu-id="09684-115">Match value.</span></span>

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

### <span data-ttu-id="09684-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="09684-116">-MatchVariable</span></span>
<span data-ttu-id="09684-117">Übereinstimmungsvariable</span><span class="sxs-lookup"><span data-stu-id="09684-117">Match Variable.</span></span>
<span data-ttu-id="09684-118">Mögliche Werte sind: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="09684-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="09684-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="09684-119">-NegateCondition</span></span>
<span data-ttu-id="09684-120">Beschreibt, ob dies eine neggate Bedingung oder kein Standardwert "false" ist.</span><span class="sxs-lookup"><span data-stu-id="09684-120">Describes if this is negate condition or not Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09684-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="09684-121">-OperatorProperty</span></span>
<span data-ttu-id="09684-122">Beschreibt den zu matching-Operator.</span><span class="sxs-lookup"><span data-stu-id="09684-122">Describes operator to be matched.</span></span>
<span data-ttu-id="09684-123">Mögliche Werte sind: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'Less Durch', 'Greater Durch', 'LessMatchOrEqual', 'Greater SelbstQual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="09684-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="09684-124">-Selector</span><span class="sxs-lookup"><span data-stu-id="09684-124">-Selector</span></span>
<span data-ttu-id="09684-125">Name des Selektors in RequestHeader oder RequestBody, der übereinstimmen soll</span><span class="sxs-lookup"><span data-stu-id="09684-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="09684-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="09684-126">-Transform</span></span>
<span data-ttu-id="09684-127">Anzuwendende Transformationen.</span><span class="sxs-lookup"><span data-stu-id="09684-127">Transforms to apply.</span></span> <span data-ttu-id="09684-128">Mögliche Werte: "Kleinbuchstaben", "Großbuchstaben", "Kürzen", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="09684-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="09684-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09684-129">CommonParameters</span></span>
<span data-ttu-id="09684-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09684-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09684-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09684-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09684-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09684-132">INPUTS</span></span>

### <span data-ttu-id="09684-133">Keine</span><span class="sxs-lookup"><span data-stu-id="09684-133">None</span></span>

## <span data-ttu-id="09684-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09684-134">OUTPUTS</span></span>

### <span data-ttu-id="09684-135">Microsoft.Azure.Commands.FrontD selbst.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="09684-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="09684-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09684-136">NOTES</span></span>

## <span data-ttu-id="09684-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09684-137">RELATED LINKS</span></span>

[<span data-ttu-id="09684-138">New-AzFrontDneuWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="09684-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
