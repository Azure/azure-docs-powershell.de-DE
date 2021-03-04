---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940344"
---
# <span data-ttu-id="ac83b-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="ac83b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac83b-102">SYNOPSIS</span></span>
<span data-ttu-id="ac83b-103">Ruft den Neuschreibregelsatz eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="ac83b-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="ac83b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac83b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac83b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac83b-105">DESCRIPTION</span></span>
<span data-ttu-id="ac83b-106">Ruft den Neuschreibregelsatz eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="ac83b-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="ac83b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac83b-107">EXAMPLES</span></span>

### <span data-ttu-id="ac83b-108">Beispiel 1: Einen bestimmten Regelsatz zum Neuschreiben erhalten</span><span class="sxs-lookup"><span data-stu-id="ac83b-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="ac83b-109">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ac83b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="ac83b-110">Der zweite Befehl ruft den Neuschreibregelsatz mit dem Namen RuleSet01 aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ac83b-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="ac83b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ac83b-111">PARAMETERS</span></span>

### <span data-ttu-id="ac83b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac83b-112">-ApplicationGateway</span></span>
<span data-ttu-id="ac83b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac83b-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac83b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac83b-114">-DefaultProfile</span></span>
<span data-ttu-id="ac83b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac83b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac83b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ac83b-116">-Name</span></span>
<span data-ttu-id="ac83b-117">Der Name des Anwendungsgateways RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="ac83b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac83b-118">CommonParameters</span></span>
<span data-ttu-id="ac83b-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac83b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac83b-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac83b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac83b-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac83b-121">INPUTS</span></span>

### <span data-ttu-id="ac83b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac83b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac83b-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac83b-123">OUTPUTS</span></span>

### <span data-ttu-id="ac83b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="ac83b-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ac83b-125">NOTES</span></span>

## <span data-ttu-id="ac83b-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ac83b-126">RELATED LINKS</span></span>

[<span data-ttu-id="ac83b-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ac83b-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ac83b-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ac83b-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ac83b-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ac83b-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="ac83b-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ac83b-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="ac83b-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac83b-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
