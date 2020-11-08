---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009050"
---
# <span data-ttu-id="b714d-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b714d-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b714d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b714d-102">SYNOPSIS</span></span>
<span data-ttu-id="b714d-103">Ändert einen Regelsatz für das erneute Schreiben für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b714d-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="b714d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b714d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b714d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b714d-105">DESCRIPTION</span></span>
<span data-ttu-id="b714d-106">Das Cmdlet " **Satz-AzApplicationGatewayRewriteRuleSet** " ändert eine Anforderungs Routingregel.</span><span class="sxs-lookup"><span data-stu-id="b714d-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="b714d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b714d-107">EXAMPLES</span></span>

### <span data-ttu-id="b714d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b714d-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="b714d-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b714d-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b714d-110">Der zweite Befehl ändert den Regelsatz für das erneute Schreiben für das Anwendungsgateway, um die in der $Rule Variablen angegebenen Regeln zum Umschreiben zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b714d-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="b714d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b714d-111">PARAMETERS</span></span>

### <span data-ttu-id="b714d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b714d-112">-ApplicationGateway</span></span>
<span data-ttu-id="b714d-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b714d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b714d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b714d-114">-DefaultProfile</span></span>
<span data-ttu-id="b714d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b714d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b714d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b714d-116">-Name</span></span>
<span data-ttu-id="b714d-117">Der Name des RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b714d-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="b714d-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="b714d-118">-RewriteRule</span></span>
<span data-ttu-id="b714d-119">Liste der Regeln zum Umschreiben</span><span class="sxs-lookup"><span data-stu-id="b714d-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="b714d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b714d-120">CommonParameters</span></span>
<span data-ttu-id="b714d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b714d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b714d-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b714d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b714d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b714d-123">INPUTS</span></span>

### <span data-ttu-id="b714d-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b714d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b714d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b714d-125">OUTPUTS</span></span>

### <span data-ttu-id="b714d-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b714d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b714d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b714d-127">NOTES</span></span>

## <span data-ttu-id="b714d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b714d-128">RELATED LINKS</span></span>

[<span data-ttu-id="b714d-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b714d-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b714d-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b714d-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b714d-131">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b714d-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b714d-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b714d-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b714d-133">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b714d-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b714d-134">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b714d-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b714d-135">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b714d-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
