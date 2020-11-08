---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009161"
---
# <span data-ttu-id="11fcd-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="11fcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="11fcd-103">Fügt einem Anwendungsgateway eine Regel Satz umschreiben hinzu.</span><span class="sxs-lookup"><span data-stu-id="11fcd-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="11fcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11fcd-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11fcd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="11fcd-106">Das Cmdlet " **Add-AzApplicationGatewayRewriteRuleSet** " fügt einem Anwendungsgateway eine umschreibungs Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="11fcd-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="11fcd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11fcd-107">EXAMPLES</span></span>

### <span data-ttu-id="11fcd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11fcd-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="11fcd-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="11fcd-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="11fcd-110">Mit dem zweiten Befehl wird die Regel für das erneute Schreiben zum Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="11fcd-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="11fcd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="11fcd-111">PARAMETERS</span></span>

### <span data-ttu-id="11fcd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fcd-112">-ApplicationGateway</span></span>
<span data-ttu-id="11fcd-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fcd-113">The applicationGateway</span></span>

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

### <span data-ttu-id="11fcd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fcd-114">-DefaultProfile</span></span>
<span data-ttu-id="11fcd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11fcd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11fcd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="11fcd-116">-Name</span></span>
<span data-ttu-id="11fcd-117">Der Name des RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="11fcd-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="11fcd-118">-RewriteRule</span></span>
<span data-ttu-id="11fcd-119">Liste der Regeln zum Umschreiben</span><span class="sxs-lookup"><span data-stu-id="11fcd-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="11fcd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fcd-120">CommonParameters</span></span>
<span data-ttu-id="11fcd-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11fcd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fcd-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11fcd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fcd-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11fcd-123">INPUTS</span></span>

### <span data-ttu-id="11fcd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fcd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11fcd-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11fcd-125">OUTPUTS</span></span>

### <span data-ttu-id="11fcd-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fcd-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11fcd-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="11fcd-127">NOTES</span></span>

## <span data-ttu-id="11fcd-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11fcd-128">RELATED LINKS</span></span>

[<span data-ttu-id="11fcd-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="11fcd-130">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="11fcd-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="11fcd-132">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="11fcd-133">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="11fcd-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="11fcd-134">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="11fcd-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="11fcd-135">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fcd-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
