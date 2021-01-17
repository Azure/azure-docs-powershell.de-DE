---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379376"
---
# <span data-ttu-id="83ebf-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="83ebf-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="83ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="83ebf-103">Erstellt eine Neuschreibungsregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="83ebf-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="83ebf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83ebf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83ebf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="83ebf-106">**Das Cmdlet "New-AzApplicationGatewayRewriteRule"** erstellt eine Neuschreibungsregel für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="83ebf-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="83ebf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="83ebf-108">Beispiel 1: Erstellen einer Neuschreibregel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="83ebf-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="83ebf-109">Dieser Befehl erstellt eine Neuschreibungsregel namens "Regel1" und speichert das Ergebnis in der Variablen namens $rule.</span><span class="sxs-lookup"><span data-stu-id="83ebf-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="83ebf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83ebf-110">PARAMETERS</span></span>

### <span data-ttu-id="83ebf-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-111">-ActionSet</span></span>
<span data-ttu-id="83ebf-112">ActionSet der Neuschreibregel</span><span class="sxs-lookup"><span data-stu-id="83ebf-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="83ebf-113">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="83ebf-113">-Condition</span></span>
<span data-ttu-id="83ebf-114">Bedingung für die auszuführende Neuschreibregel</span><span class="sxs-lookup"><span data-stu-id="83ebf-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="83ebf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ebf-115">-DefaultProfile</span></span>
<span data-ttu-id="83ebf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83ebf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ebf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="83ebf-117">-Name</span></span>
<span data-ttu-id="83ebf-118">Der Name der Neuschreibung</span><span class="sxs-lookup"><span data-stu-id="83ebf-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="83ebf-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="83ebf-119">-RuleSequence</span></span>
<span data-ttu-id="83ebf-120">Die Regelreihenfolge dieser Neuschreibungsregel im Neuschreibregelsatz</span><span class="sxs-lookup"><span data-stu-id="83ebf-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="83ebf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ebf-121">CommonParameters</span></span>
<span data-ttu-id="83ebf-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ebf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ebf-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ebf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ebf-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83ebf-124">INPUTS</span></span>

### <span data-ttu-id="83ebf-125">Keine</span><span class="sxs-lookup"><span data-stu-id="83ebf-125">None</span></span>

## <span data-ttu-id="83ebf-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83ebf-126">OUTPUTS</span></span>

### <span data-ttu-id="83ebf-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="83ebf-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="83ebf-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="83ebf-128">NOTES</span></span>

## <span data-ttu-id="83ebf-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="83ebf-129">RELATED LINKS</span></span>

[<span data-ttu-id="83ebf-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="83ebf-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="83ebf-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="83ebf-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="83ebf-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="83ebf-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="83ebf-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="83ebf-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="83ebf-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
