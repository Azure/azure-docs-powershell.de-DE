---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: d657c769a32d7c042a12a56571343885c526eea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933864"
---
# <span data-ttu-id="897dc-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897dc-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="897dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="897dc-102">SYNOPSIS</span></span>
<span data-ttu-id="897dc-103">Fügt einem Anwendungsgateway eine Neuschreibungsregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="897dc-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="897dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="897dc-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="897dc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="897dc-105">DESCRIPTION</span></span>
<span data-ttu-id="897dc-106">Das **Add-AzApplicationGatewayRewriteRuleSet-Cmdlet** fügt einem Anwendungsgateway eine Neuschreibregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="897dc-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="897dc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="897dc-107">EXAMPLES</span></span>

### <span data-ttu-id="897dc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="897dc-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="897dc-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="897dc-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="897dc-110">Der zweite Befehl fügt dem Anwendungsgateway die neu festgelegte Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="897dc-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="897dc-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="897dc-111">PARAMETERS</span></span>

### <span data-ttu-id="897dc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897dc-112">-ApplicationGateway</span></span>
<span data-ttu-id="897dc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897dc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="897dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897dc-114">-DefaultProfile</span></span>
<span data-ttu-id="897dc-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="897dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897dc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="897dc-116">-Name</span></span>
<span data-ttu-id="897dc-117">Der Name des RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="897dc-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="897dc-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="897dc-118">-RewriteRule</span></span>
<span data-ttu-id="897dc-119">Liste der Neuschreibregeln</span><span class="sxs-lookup"><span data-stu-id="897dc-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="897dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897dc-120">CommonParameters</span></span>
<span data-ttu-id="897dc-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897dc-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="897dc-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897dc-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="897dc-123">INPUTS</span></span>

### <span data-ttu-id="897dc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897dc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="897dc-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="897dc-125">OUTPUTS</span></span>

### <span data-ttu-id="897dc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897dc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="897dc-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="897dc-127">NOTES</span></span>

## <span data-ttu-id="897dc-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="897dc-128">RELATED LINKS</span></span>

[<span data-ttu-id="897dc-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897dc-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="897dc-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897dc-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="897dc-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897dc-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="897dc-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897dc-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="897dc-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="897dc-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="897dc-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="897dc-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="897dc-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="897dc-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
