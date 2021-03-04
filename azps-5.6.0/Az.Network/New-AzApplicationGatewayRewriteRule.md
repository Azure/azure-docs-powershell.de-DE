---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: a69f5a3a1da8ec2ac8937793051f0361bf5e0681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948563"
---
# <span data-ttu-id="b6f7e-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b6f7e-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="b6f7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f7e-103">Erstellt eine Neuschreibungsregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="b6f7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6f7e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6f7e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f7e-106">**Das Cmdlet New-AzApplicationGatewayRewriteRule** erstellt eine Neuschreibregel für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="b6f7e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f7e-108">Beispiel 1: Erstellen einer Neuschreibregel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b6f7e-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="b6f7e-109">Mit diesem Befehl wird eine Regel mit dem Namen Regel1 erstellt und das Ergebnis in der Variablen namens $rule.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="b6f7e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b6f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f7e-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-111">-ActionSet</span></span>
<span data-ttu-id="b6f7e-112">ActionSet der Neuschreibungsregel</span><span class="sxs-lookup"><span data-stu-id="b6f7e-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f7e-113">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="b6f7e-113">-Condition</span></span>
<span data-ttu-id="b6f7e-114">Bedingung für die Ausführung der Neuschreibregel</span><span class="sxs-lookup"><span data-stu-id="b6f7e-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f7e-115">-DefaultProfile</span></span>
<span data-ttu-id="b6f7e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f7e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b6f7e-117">-Name</span></span>
<span data-ttu-id="b6f7e-118">Der Name des RewriteRule</span><span class="sxs-lookup"><span data-stu-id="b6f7e-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="b6f7e-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="b6f7e-119">-RuleSequence</span></span>
<span data-ttu-id="b6f7e-120">Die Regelreihenfolge dieser Neuschreibungsregel im Neuschreibregelsatz</span><span class="sxs-lookup"><span data-stu-id="b6f7e-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="b6f7e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f7e-121">CommonParameters</span></span>
<span data-ttu-id="b6f7e-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f7e-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f7e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f7e-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6f7e-124">INPUTS</span></span>

### <span data-ttu-id="b6f7e-125">Keine</span><span class="sxs-lookup"><span data-stu-id="b6f7e-125">None</span></span>

## <span data-ttu-id="b6f7e-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6f7e-126">OUTPUTS</span></span>

### <span data-ttu-id="b6f7e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b6f7e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="b6f7e-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b6f7e-128">NOTES</span></span>

## <span data-ttu-id="b6f7e-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b6f7e-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6f7e-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b6f7e-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b6f7e-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b6f7e-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b6f7e-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b6f7e-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b6f7e-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b6f7e-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f7e-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
