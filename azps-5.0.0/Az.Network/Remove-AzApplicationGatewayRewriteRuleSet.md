---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303645"
---
# <span data-ttu-id="f0a74-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f0a74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0a74-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a74-103">Entfernt eine Neuschreiben-Regelgruppe aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f0a74-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="f0a74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0a74-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0a74-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a74-106">Das Cmdlet " **Remove-AzApplicationGatewayRewriteRuleSet** " entfernt eine Rewrite-Regelgruppe aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f0a74-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="f0a74-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0a74-107">EXAMPLES</span></span>

### <span data-ttu-id="f0a74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0a74-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="f0a74-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f0a74-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f0a74-110">Der zweite Befehl entfernt den Rewrite-Regelsatz mit dem Namen RuleSet02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f0a74-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f0a74-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0a74-111">PARAMETERS</span></span>

### <span data-ttu-id="f0a74-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0a74-112">-ApplicationGateway</span></span>
<span data-ttu-id="f0a74-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0a74-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f0a74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a74-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a74-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0a74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a74-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f0a74-116">-Name</span></span>
<span data-ttu-id="f0a74-117">Der Name des Anwendungsgateway-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f0a74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a74-118">CommonParameters</span></span>
<span data-ttu-id="f0a74-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a74-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a74-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a74-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0a74-121">INPUTS</span></span>

### <span data-ttu-id="f0a74-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0a74-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0a74-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0a74-123">OUTPUTS</span></span>

### <span data-ttu-id="f0a74-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0a74-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0a74-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0a74-125">NOTES</span></span>

## <span data-ttu-id="f0a74-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0a74-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0a74-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0a74-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0a74-129">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0a74-130">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0a74-131">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f0a74-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f0a74-132">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f0a74-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="f0a74-133">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0a74-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
