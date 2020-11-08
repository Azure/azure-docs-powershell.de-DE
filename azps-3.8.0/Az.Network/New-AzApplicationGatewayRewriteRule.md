---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004995"
---
# <span data-ttu-id="31174-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="31174-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="31174-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31174-102">SYNOPSIS</span></span>
<span data-ttu-id="31174-103">Erstellt eine Rewrite-Regel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="31174-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="31174-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31174-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31174-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31174-105">DESCRIPTION</span></span>
<span data-ttu-id="31174-106">**Das Cmdlet New-AzApplicationGatewayRewriteRule** erstellt eine Rewrite-Regel für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="31174-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="31174-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31174-107">EXAMPLES</span></span>

### <span data-ttu-id="31174-108">Beispiel 1: Erstellen einer Rewrite-Regel für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="31174-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="31174-109">Dieser Befehl erstellt eine Rewrite-Regel mit dem Namen rule1 und speichert das Ergebnis in der Variablen mit dem Namen $Rule.</span><span class="sxs-lookup"><span data-stu-id="31174-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="31174-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="31174-110">PARAMETERS</span></span>

### <span data-ttu-id="31174-111">-Actionset</span><span class="sxs-lookup"><span data-stu-id="31174-111">-ActionSet</span></span>
<span data-ttu-id="31174-112">Aktionsset der Regel zum Umschreiben</span><span class="sxs-lookup"><span data-stu-id="31174-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="31174-113">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="31174-113">-Condition</span></span>
<span data-ttu-id="31174-114">Bedingung für die Ausführung der umschreibungs Regel</span><span class="sxs-lookup"><span data-stu-id="31174-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="31174-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31174-115">-DefaultProfile</span></span>
<span data-ttu-id="31174-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31174-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31174-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31174-117">-Name</span></span>
<span data-ttu-id="31174-118">Der Name des RewriteRule</span><span class="sxs-lookup"><span data-stu-id="31174-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="31174-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="31174-119">-RuleSequence</span></span>
<span data-ttu-id="31174-120">Die Regelreihenfolge dieser umschreibungs Regel in der Regelgruppe "neu schreiben"</span><span class="sxs-lookup"><span data-stu-id="31174-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="31174-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31174-121">CommonParameters</span></span>
<span data-ttu-id="31174-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31174-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31174-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31174-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31174-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31174-124">INPUTS</span></span>

### <span data-ttu-id="31174-125">Keine</span><span class="sxs-lookup"><span data-stu-id="31174-125">None</span></span>

## <span data-ttu-id="31174-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31174-126">OUTPUTS</span></span>

### <span data-ttu-id="31174-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="31174-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="31174-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="31174-128">NOTES</span></span>

## <span data-ttu-id="31174-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31174-129">RELATED LINKS</span></span>

[<span data-ttu-id="31174-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31174-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31174-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31174-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31174-132">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31174-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31174-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31174-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31174-134">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31174-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31174-135">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="31174-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="31174-136">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="31174-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
