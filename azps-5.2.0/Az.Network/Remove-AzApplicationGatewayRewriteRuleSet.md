---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298888"
---
# <span data-ttu-id="9ecae-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ecae-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9ecae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ecae-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecae-103">Entfernt einen Neuschreibregelsatz von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9ecae-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="9ecae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ecae-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ecae-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ecae-105">DESCRIPTION</span></span>
<span data-ttu-id="9ecae-106">Das **Cmdlet "Remove-AzApplicationGatewayRewriteRuleSet"** entfernt einen Neuschreibregelsatz von einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9ecae-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="9ecae-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ecae-107">EXAMPLES</span></span>

### <span data-ttu-id="9ecae-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ecae-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="9ecae-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="9ecae-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9ecae-110">Mit dem zweiten Befehl wird der Neuschreibregelsatz mit dem Namen "RuleSet02" aus dem Anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9ecae-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9ecae-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ecae-111">PARAMETERS</span></span>

### <span data-ttu-id="9ecae-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecae-112">-ApplicationGateway</span></span>
<span data-ttu-id="9ecae-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecae-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9ecae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecae-114">-DefaultProfile</span></span>
<span data-ttu-id="9ecae-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ecae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ecae-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9ecae-116">-Name</span></span>
<span data-ttu-id="9ecae-117">Der Name des Anwendungsgateways "RewriteRuleSet"</span><span class="sxs-lookup"><span data-stu-id="9ecae-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9ecae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecae-118">CommonParameters</span></span>
<span data-ttu-id="9ecae-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ecae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecae-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ecae-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecae-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ecae-121">INPUTS</span></span>

### <span data-ttu-id="9ecae-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecae-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ecae-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ecae-123">OUTPUTS</span></span>

### <span data-ttu-id="9ecae-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ecae-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ecae-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ecae-125">NOTES</span></span>

## <span data-ttu-id="9ecae-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ecae-126">RELATED LINKS</span></span>

[<span data-ttu-id="9ecae-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ecae-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9ecae-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ecae-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9ecae-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ecae-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9ecae-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ecae-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9ecae-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9ecae-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9ecae-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9ecae-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9ecae-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ecae-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
