---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172985"
---
# <span data-ttu-id="0a065-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a065-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="0a065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a065-102">SYNOPSIS</span></span>
<span data-ttu-id="0a065-103">Fügt einem Anwendungsgateway einen Neuschreibregelsatz hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a065-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="0a065-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a065-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a065-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a065-105">DESCRIPTION</span></span>
<span data-ttu-id="0a065-106">Das **Cmdlet "Add-AzApplicationGatewayRewriteRuleSet"** fügt einem Anwendungsgateway einen Neuschreibregelsatz hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a065-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="0a065-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a065-107">EXAMPLES</span></span>

### <span data-ttu-id="0a065-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a065-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="0a065-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="0a065-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0a065-110">Der zweite Befehl fügt dem Anwendungsgateway den Neuschreibregelsatz hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a065-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="0a065-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a065-111">PARAMETERS</span></span>

### <span data-ttu-id="0a065-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a065-112">-ApplicationGateway</span></span>
<span data-ttu-id="0a065-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a065-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0a065-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a065-114">-DefaultProfile</span></span>
<span data-ttu-id="0a065-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a065-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a065-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0a065-116">-Name</span></span>
<span data-ttu-id="0a065-117">Der Name des RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a065-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="0a065-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="0a065-118">-RewriteRule</span></span>
<span data-ttu-id="0a065-119">Liste der Neuschreibungsregeln</span><span class="sxs-lookup"><span data-stu-id="0a065-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="0a065-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a065-120">CommonParameters</span></span>
<span data-ttu-id="0a065-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a065-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a065-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a065-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a065-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a065-123">INPUTS</span></span>

### <span data-ttu-id="0a065-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a065-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a065-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a065-125">OUTPUTS</span></span>

### <span data-ttu-id="0a065-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a065-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a065-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a065-127">NOTES</span></span>

## <span data-ttu-id="0a065-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a065-128">RELATED LINKS</span></span>

[<span data-ttu-id="0a065-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a065-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0a065-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a065-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0a065-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a065-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0a065-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a065-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0a065-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0a065-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="0a065-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a065-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="0a065-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a065-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
