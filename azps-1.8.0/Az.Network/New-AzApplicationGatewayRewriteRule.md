---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 9fdbf6f7cd88774c2d14d079201993f6a324ace5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660596"
---
# <span data-ttu-id="e2e64-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e2e64-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="e2e64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2e64-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e64-103">Erstellt eine Rewrite-Regel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e2e64-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="e2e64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2e64-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e64-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e64-106">**Das Cmdlet New-AzApplicationGatewayRewriteRule** erstellt eine Rewrite-Regel für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="e2e64-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="e2e64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2e64-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e64-108">Beispiel 1: Erstellen einer Rewrite-Regel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e2e64-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="e2e64-109">Dieser Befehl erstellt eine Rewrite-Regel mit dem Namen rule1 und speichert das Ergebnis in der Variablen mit dem Namen $Rule.</span><span class="sxs-lookup"><span data-stu-id="e2e64-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="e2e64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e64-110">PARAMETERS</span></span>

### <span data-ttu-id="e2e64-111">-Actionset</span><span class="sxs-lookup"><span data-stu-id="e2e64-111">-ActionSet</span></span>
<span data-ttu-id="e2e64-112">Aktionsset der Regel zum Umschreiben</span><span class="sxs-lookup"><span data-stu-id="e2e64-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="e2e64-113">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="e2e64-113">-Condition</span></span>
<span data-ttu-id="e2e64-114">Bedingung für die Ausführung der umschreibungs Regel</span><span class="sxs-lookup"><span data-stu-id="e2e64-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="e2e64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e64-115">-DefaultProfile</span></span>
<span data-ttu-id="e2e64-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2e64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e64-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e2e64-117">-Name</span></span>
<span data-ttu-id="e2e64-118">Der Name des RewriteRule</span><span class="sxs-lookup"><span data-stu-id="e2e64-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="e2e64-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="e2e64-119">-RuleSequence</span></span>
<span data-ttu-id="e2e64-120">Die Regelreihenfolge dieser umschreibungs Regel in der Regelgruppe "neu schreiben"</span><span class="sxs-lookup"><span data-stu-id="e2e64-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="e2e64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e64-121">CommonParameters</span></span>
<span data-ttu-id="e2e64-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e64-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e64-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2e64-124">INPUTS</span></span>

### <span data-ttu-id="e2e64-125">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e64-125">None</span></span>

## <span data-ttu-id="e2e64-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2e64-126">OUTPUTS</span></span>

### <span data-ttu-id="e2e64-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e2e64-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="e2e64-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2e64-128">NOTES</span></span>

## <span data-ttu-id="e2e64-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2e64-129">RELATED LINKS</span></span>

[<span data-ttu-id="e2e64-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2e64-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e2e64-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2e64-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e2e64-132">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2e64-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e2e64-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2e64-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e2e64-134">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2e64-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e2e64-135">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e2e64-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e2e64-136">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2e64-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
