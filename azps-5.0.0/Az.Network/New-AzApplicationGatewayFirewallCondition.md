---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180158"
---
# <span data-ttu-id="1fc98-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1fc98-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="1fc98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fc98-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc98-103">Erstellt eine übereinstimmungsbedingung für die benutzerdefinierte Regel</span><span class="sxs-lookup"><span data-stu-id="1fc98-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="1fc98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fc98-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fc98-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc98-106">Das **AzApplicationGatewayFirewallCondition** erstellt eine übereinstimmungsbedingung für die benutzerdefinierte Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1fc98-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="1fc98-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fc98-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc98-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fc98-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="1fc98-109">Der Befehl erstellt eine neue übereinstimmungsbedingung mithilfe der in der $Variable definierten Übereinstimmungsvariablen, der Operator ist Contains und die Negations Bedingung ist falsch, umgeht einschließlich klein-und Zuschneiden, der Übereinstimmungs Wert ist ABC und CDE.</span><span class="sxs-lookup"><span data-stu-id="1fc98-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="1fc98-110">Die neue übereinstimmungsbedingung wird in $Condition gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1fc98-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="1fc98-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fc98-111">PARAMETERS</span></span>

### <span data-ttu-id="1fc98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc98-112">-DefaultProfile</span></span>
<span data-ttu-id="1fc98-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fc98-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fc98-114">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="1fc98-114">-MatchValue</span></span>
<span data-ttu-id="1fc98-115">Übereinstimmungs Wert.</span><span class="sxs-lookup"><span data-stu-id="1fc98-115">Match value.</span></span>

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

### <span data-ttu-id="1fc98-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="1fc98-116">-MatchVariable</span></span>
<span data-ttu-id="1fc98-117">Liste der Übereinstimmungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="1fc98-117">List of match variables.</span></span>

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

### <span data-ttu-id="1fc98-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="1fc98-118">-NegationCondition</span></span>
<span data-ttu-id="1fc98-119">Beschreibt, ob es sich um eine Negations Bedingung handelt.</span><span class="sxs-lookup"><span data-stu-id="1fc98-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="1fc98-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="1fc98-120">-Operator</span></span>
<span data-ttu-id="1fc98-121">Beschreibt den Operator, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fc98-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="1fc98-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="1fc98-122">-Transform</span></span>
<span data-ttu-id="1fc98-123">Liste der Transformationen</span><span class="sxs-lookup"><span data-stu-id="1fc98-123">List of transforms.</span></span>

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

### <span data-ttu-id="1fc98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc98-124">CommonParameters</span></span>
<span data-ttu-id="1fc98-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc98-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc98-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc98-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fc98-127">INPUTS</span></span>

### <span data-ttu-id="1fc98-128">Keine</span><span class="sxs-lookup"><span data-stu-id="1fc98-128">None</span></span>

## <span data-ttu-id="1fc98-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fc98-129">OUTPUTS</span></span>

### <span data-ttu-id="1fc98-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1fc98-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="1fc98-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fc98-131">NOTES</span></span>

## <span data-ttu-id="1fc98-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fc98-132">RELATED LINKS</span></span>
