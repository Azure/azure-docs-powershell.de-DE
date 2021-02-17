---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172745"
---
# <span data-ttu-id="b2269-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b2269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2269-102">SYNOPSIS</span></span>
<span data-ttu-id="b2269-103">Erstellt eine Anforderungsroutingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b2269-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="b2269-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2269-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2269-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2269-105">DESCRIPTION</span></span>
<span data-ttu-id="b2269-106">**Das Cmdlet "New-AzApplicationGatewayRewriteRuleSet"** erstellt einen Neuschreibregelsatz für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b2269-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="b2269-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2269-107">EXAMPLES</span></span>

### <span data-ttu-id="b2269-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2269-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="b2269-109">Mit diesem Befehl wird ein Neuschreibregelsatz namens "ruleset1" erstellt und das Ergebnis in der Variablen namens "$ruleset.</span><span class="sxs-lookup"><span data-stu-id="b2269-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="b2269-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2269-110">PARAMETERS</span></span>

### <span data-ttu-id="b2269-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2269-111">-DefaultProfile</span></span>
<span data-ttu-id="b2269-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2269-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2269-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b2269-113">-Name</span></span>
<span data-ttu-id="b2269-114">Der Name des RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="b2269-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="b2269-115">-RewriteRule</span></span>
<span data-ttu-id="b2269-116">Liste der Neuschreibungsregeln</span><span class="sxs-lookup"><span data-stu-id="b2269-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2269-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2269-117">CommonParameters</span></span>
<span data-ttu-id="b2269-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2269-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2269-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2269-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2269-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2269-120">INPUTS</span></span>

### <span data-ttu-id="b2269-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b2269-121">None</span></span>

## <span data-ttu-id="b2269-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2269-122">OUTPUTS</span></span>

### <span data-ttu-id="b2269-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b2269-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2269-124">NOTES</span></span>

## <span data-ttu-id="b2269-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2269-125">RELATED LINKS</span></span>

[<span data-ttu-id="b2269-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b2269-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b2269-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b2269-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2269-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b2269-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b2269-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b2269-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b2269-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b2269-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2269-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
