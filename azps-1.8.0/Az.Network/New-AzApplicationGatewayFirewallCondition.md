---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: ee7f6f2b824041cf56b27c34dc70358c4229e527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660630"
---
# <span data-ttu-id="dbe95-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="dbe95-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="dbe95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbe95-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe95-103">Erstellt eine übereinstimmungsbedingung für die benutzerdefinierte Regel</span><span class="sxs-lookup"><span data-stu-id="dbe95-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="dbe95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbe95-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbe95-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbe95-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe95-106">Das **AzApplicationGatewayFirewallCondition** erstellt eine übereinstimmungsbedingung für die benutzerdefinierte Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="dbe95-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="dbe95-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbe95-107">EXAMPLES</span></span>

### <span data-ttu-id="dbe95-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbe95-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzureRmApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="dbe95-109">Der Befehl erstellt eine neue übereinstimmungsbedingung mithilfe der in der $Variable definierten Übereinstimmungsvariablen, der Operator ist Contains und die Negations Bedingung ist falsch, umgeht einschließlich klein-und Zuschneiden, der Übereinstimmungs Wert ist ABC und CDE.</span><span class="sxs-lookup"><span data-stu-id="dbe95-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="dbe95-110">Die neue übereinstimmungsbedingung wird in $Condition gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dbe95-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="dbe95-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbe95-111">PARAMETERS</span></span>

### <span data-ttu-id="dbe95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe95-112">-DefaultProfile</span></span>
<span data-ttu-id="dbe95-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbe95-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbe95-114">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="dbe95-114">-MatchValue</span></span>
<span data-ttu-id="dbe95-115">Übereinstimmungs Wert.</span><span class="sxs-lookup"><span data-stu-id="dbe95-115">Match value.</span></span>

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

### <span data-ttu-id="dbe95-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="dbe95-116">-MatchVariable</span></span>
<span data-ttu-id="dbe95-117">Liste der Übereinstimmungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="dbe95-117">List of match variables.</span></span>

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

### <span data-ttu-id="dbe95-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="dbe95-118">-NegationCondition</span></span>
<span data-ttu-id="dbe95-119">Beschreibt, ob es sich um eine Negations Bedingung handelt.</span><span class="sxs-lookup"><span data-stu-id="dbe95-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="dbe95-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="dbe95-120">-Operator</span></span>
<span data-ttu-id="dbe95-121">Beschreibt den Operator, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbe95-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="dbe95-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="dbe95-122">-Transform</span></span>
<span data-ttu-id="dbe95-123">Liste der Transformationen</span><span class="sxs-lookup"><span data-stu-id="dbe95-123">List of transforms.</span></span>

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

### <span data-ttu-id="dbe95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe95-124">CommonParameters</span></span>
<span data-ttu-id="dbe95-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe95-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe95-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe95-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbe95-127">INPUTS</span></span>

### <span data-ttu-id="dbe95-128">Keine</span><span class="sxs-lookup"><span data-stu-id="dbe95-128">None</span></span>

## <span data-ttu-id="dbe95-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbe95-129">OUTPUTS</span></span>

### <span data-ttu-id="dbe95-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="dbe95-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="dbe95-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbe95-131">NOTES</span></span>

## <span data-ttu-id="dbe95-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbe95-132">RELATED LINKS</span></span>
