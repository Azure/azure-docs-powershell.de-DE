---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946492"
---
# <span data-ttu-id="1ebfb-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1ebfb-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="1ebfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ebfb-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebfb-103">Erstellt eine Übereinstimmungsbedingung für eine benutzerdefinierte Regel</span><span class="sxs-lookup"><span data-stu-id="1ebfb-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="1ebfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ebfb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ebfb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ebfb-105">DESCRIPTION</span></span>
<span data-ttu-id="1ebfb-106">Die **New-AzApplicationGatewayFirewallCondition** erstellt eine Übereinstimmungsbedingung für benutzerdefinierte Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="1ebfb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ebfb-107">EXAMPLES</span></span>

### <span data-ttu-id="1ebfb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ebfb-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="1ebfb-109">Der Befehl erstellt eine neue Übereinstimmungsbedingung mit der im $variable definierten Übereinstimmungsvariablen, der Operator ist Enthält und negation bedingung ist false, Transfroms einschließlich Kleinbuchstaben und Kürzen, der Übereinstimmungswert ist abc und cde.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="1ebfb-110">Die neue Übereinstimmungsbedingung wird in $condition.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="1ebfb-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ebfb-111">PARAMETERS</span></span>

### <span data-ttu-id="1ebfb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebfb-112">-DefaultProfile</span></span>
<span data-ttu-id="1ebfb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ebfb-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="1ebfb-114">-MatchValue</span></span>
<span data-ttu-id="1ebfb-115">Übereinstimmungswert.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebfb-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="1ebfb-116">-MatchVariable</span></span>
<span data-ttu-id="1ebfb-117">Liste der Übereinstimmungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebfb-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="1ebfb-118">-NegationCondition</span></span>
<span data-ttu-id="1ebfb-119">Beschreibt, ob es sich um eine neggate Bedingung handelt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="1ebfb-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="1ebfb-120">-Operator</span></span>
<span data-ttu-id="1ebfb-121">Beschreibt den operator, der übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebfb-122">-Transformieren</span><span class="sxs-lookup"><span data-stu-id="1ebfb-122">-Transform</span></span>
<span data-ttu-id="1ebfb-123">Liste der Transformationen.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebfb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebfb-124">CommonParameters</span></span>
<span data-ttu-id="1ebfb-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebfb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebfb-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ebfb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebfb-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ebfb-127">INPUTS</span></span>

### <span data-ttu-id="1ebfb-128">Keine</span><span class="sxs-lookup"><span data-stu-id="1ebfb-128">None</span></span>

## <span data-ttu-id="1ebfb-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ebfb-129">OUTPUTS</span></span>

### <span data-ttu-id="1ebfb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1ebfb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="1ebfb-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ebfb-131">NOTES</span></span>

## <span data-ttu-id="1ebfb-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ebfb-132">RELATED LINKS</span></span>
