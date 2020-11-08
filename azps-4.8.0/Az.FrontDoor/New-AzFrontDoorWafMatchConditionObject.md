---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007960"
---
# <span data-ttu-id="748a1-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="748a1-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="748a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="748a1-102">SYNOPSIS</span></span>
<span data-ttu-id="748a1-103">Erstellen eines MatchCondition-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="748a1-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="748a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="748a1-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="748a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="748a1-105">DESCRIPTION</span></span>
<span data-ttu-id="748a1-106">Erstellen eines MatchCondition-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="748a1-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="748a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="748a1-107">EXAMPLES</span></span>

### <span data-ttu-id="748a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="748a1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="748a1-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="748a1-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="748a1-110">Erstellen eines MatchCondition-Objekts</span><span class="sxs-lookup"><span data-stu-id="748a1-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="748a1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="748a1-111">PARAMETERS</span></span>

### <span data-ttu-id="748a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="748a1-112">-DefaultProfile</span></span>
<span data-ttu-id="748a1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="748a1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="748a1-114">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="748a1-114">-MatchValue</span></span>
<span data-ttu-id="748a1-115">Übereinstimmungs Wert.</span><span class="sxs-lookup"><span data-stu-id="748a1-115">Match value.</span></span>

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

### <span data-ttu-id="748a1-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="748a1-116">-MatchVariable</span></span>
<span data-ttu-id="748a1-117">Variable vergleichen.</span><span class="sxs-lookup"><span data-stu-id="748a1-117">Match Variable.</span></span>
<span data-ttu-id="748a1-118">Mögliche Werte sind: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' postargs ', ' RequestUri ', ' RequestHeader ', ' RequestBody ', ' SocketAddr '</span><span class="sxs-lookup"><span data-stu-id="748a1-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="748a1-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="748a1-119">-NegateCondition</span></span>
<span data-ttu-id="748a1-120">Beschreibt, ob es sich um eine Negations Bedingung handelt oder ob der Standardwert falsch ist.</span><span class="sxs-lookup"><span data-stu-id="748a1-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="748a1-121">-Operatorproperty</span><span class="sxs-lookup"><span data-stu-id="748a1-121">-OperatorProperty</span></span>
<span data-ttu-id="748a1-122">Beschreibt den Operator, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="748a1-122">Describes operator to be matched.</span></span>
<span data-ttu-id="748a1-123">Mögliche Werte sind: "Any", "IPMatch", "geomatch", "gleich", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "beginntmitder", "endsWith", "regex"</span><span class="sxs-lookup"><span data-stu-id="748a1-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="748a1-124">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="748a1-124">-Selector</span></span>
<span data-ttu-id="748a1-125">Der Name des Selektors in RequestHeader oder RequestBody, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="748a1-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="748a1-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="748a1-126">-Transform</span></span>
<span data-ttu-id="748a1-127">Transformationen, die angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="748a1-127">Transforms to apply.</span></span> <span data-ttu-id="748a1-128">Mögliche Werte sind: "Kleinbuchstaben", "Großbuchstaben", "trimmen", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="748a1-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="748a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="748a1-129">CommonParameters</span></span>
<span data-ttu-id="748a1-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="748a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="748a1-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="748a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="748a1-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="748a1-132">INPUTS</span></span>

### <span data-ttu-id="748a1-133">Keine</span><span class="sxs-lookup"><span data-stu-id="748a1-133">None</span></span>

## <span data-ttu-id="748a1-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="748a1-134">OUTPUTS</span></span>

### <span data-ttu-id="748a1-135">Microsoft. Azure. Commands. Haustür. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="748a1-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="748a1-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="748a1-136">NOTES</span></span>

## <span data-ttu-id="748a1-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="748a1-137">RELATED LINKS</span></span>

[<span data-ttu-id="748a1-138">Neu – AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="748a1-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
