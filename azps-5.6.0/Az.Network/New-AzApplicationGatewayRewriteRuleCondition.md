---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 9f53ddd628b313a02cf15ce6d80097f0b916c6f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944015"
---
# <span data-ttu-id="85c57-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="85c57-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="85c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c57-102">SYNOPSIS</span></span>
<span data-ttu-id="85c57-103">Fügt dem RewriteRule für ein Anwendungsgateway eine Bedingung hinzu.</span><span class="sxs-lookup"><span data-stu-id="85c57-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="85c57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85c57-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c57-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85c57-105">DESCRIPTION</span></span>
<span data-ttu-id="85c57-106">**Das AzApplicationGatewayRewriteRuleCondition-Cmdlet** erstellt eine Neuschreibregelbedingung für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="85c57-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="85c57-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85c57-107">EXAMPLES</span></span>

### <span data-ttu-id="85c57-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85c57-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="85c57-109">Dieser Befehl erstellt eine Bedingung in einer Neuschreibregel und speichert das Ergebnis in der Variablen namens $condition.</span><span class="sxs-lookup"><span data-stu-id="85c57-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="85c57-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="85c57-110">PARAMETERS</span></span>

### <span data-ttu-id="85c57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c57-111">-DefaultProfile</span></span>
<span data-ttu-id="85c57-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85c57-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c57-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="85c57-113">-IgnoreCase</span></span>
<span data-ttu-id="85c57-114">Festlegen dieses Kennzeichens zum Ignorieren von Fällen im Muster</span><span class="sxs-lookup"><span data-stu-id="85c57-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c57-115">-Neggate</span><span class="sxs-lookup"><span data-stu-id="85c57-115">-Negate</span></span>
<span data-ttu-id="85c57-116">Festlegen dieses Kennzeichens zum Negieren der Bedingungsüberprüfung</span><span class="sxs-lookup"><span data-stu-id="85c57-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c57-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="85c57-117">-Pattern</span></span>
<span data-ttu-id="85c57-118">Muster, nach dem sie in der Variablenüberschrift suchen möchten</span><span class="sxs-lookup"><span data-stu-id="85c57-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="85c57-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="85c57-119">-Variable</span></span>
<span data-ttu-id="85c57-120">Name der Kopfzeile, die bedingungs festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="85c57-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="85c57-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c57-121">CommonParameters</span></span>
<span data-ttu-id="85c57-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c57-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="85c57-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c57-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c57-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85c57-124">INPUTS</span></span>

### <span data-ttu-id="85c57-125">Keine</span><span class="sxs-lookup"><span data-stu-id="85c57-125">None</span></span>

## <span data-ttu-id="85c57-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85c57-126">OUTPUTS</span></span>

### <span data-ttu-id="85c57-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="85c57-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="85c57-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="85c57-128">NOTES</span></span>

## <span data-ttu-id="85c57-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="85c57-129">RELATED LINKS</span></span>
[<span data-ttu-id="85c57-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c57-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="85c57-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c57-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="85c57-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c57-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="85c57-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c57-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="85c57-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c57-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="85c57-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="85c57-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="85c57-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="85c57-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
