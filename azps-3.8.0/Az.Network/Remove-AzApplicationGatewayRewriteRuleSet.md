---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995043"
---
# <span data-ttu-id="1af65-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1af65-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="1af65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1af65-102">SYNOPSIS</span></span>
<span data-ttu-id="1af65-103">Entfernt eine Neuschreiben-Regelgruppe aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1af65-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="1af65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1af65-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af65-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1af65-105">DESCRIPTION</span></span>
<span data-ttu-id="1af65-106">Das Cmdlet " **Remove-AzApplicationGatewayRewriteRuleSet** " entfernt eine Rewrite-Regelgruppe aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1af65-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="1af65-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1af65-107">EXAMPLES</span></span>

### <span data-ttu-id="1af65-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1af65-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="1af65-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1af65-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1af65-110">Der zweite Befehl entfernt den Rewrite-Regelsatz mit dem Namen RuleSet02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1af65-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1af65-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1af65-111">PARAMETERS</span></span>

### <span data-ttu-id="1af65-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af65-112">-ApplicationGateway</span></span>
<span data-ttu-id="1af65-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af65-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1af65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af65-114">-DefaultProfile</span></span>
<span data-ttu-id="1af65-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1af65-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af65-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1af65-116">-Name</span></span>
<span data-ttu-id="1af65-117">Der Name des Anwendungsgateway-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1af65-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="1af65-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af65-118">CommonParameters</span></span>
<span data-ttu-id="1af65-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af65-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af65-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af65-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af65-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1af65-121">INPUTS</span></span>

### <span data-ttu-id="1af65-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af65-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1af65-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1af65-123">OUTPUTS</span></span>

### <span data-ttu-id="1af65-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af65-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1af65-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1af65-125">NOTES</span></span>

## <span data-ttu-id="1af65-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1af65-126">RELATED LINKS</span></span>

[<span data-ttu-id="1af65-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1af65-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1af65-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1af65-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1af65-129">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1af65-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1af65-130">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1af65-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1af65-131">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1af65-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="1af65-132">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1af65-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="1af65-133">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1af65-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
