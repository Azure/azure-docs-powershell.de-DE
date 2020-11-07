---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822160"
---
# <span data-ttu-id="98364-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="98364-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="98364-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98364-102">SYNOPSIS</span></span>
<span data-ttu-id="98364-103">Erstellt eine Regelaktion zum Umschreiben für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="98364-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="98364-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98364-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98364-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98364-105">DESCRIPTION</span></span>
<span data-ttu-id="98364-106">Mit **dem Cmdlet "New-AzApplicationGatewayRewriteRuleActionSet"** wird ein Rewrite-Regel Aktionssatz für ein Azure Application-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="98364-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="98364-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98364-107">EXAMPLES</span></span>

### <span data-ttu-id="98364-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98364-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="98364-109">Mit diesem Befehl wird eine Rewrite-Regelaktion-Gruppe erstellt, und das Ergebnis wird in der Variablen mit dem Namen $Action gespeichert.</span><span class="sxs-lookup"><span data-stu-id="98364-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="98364-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="98364-110">PARAMETERS</span></span>

### <span data-ttu-id="98364-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98364-111">-DefaultProfile</span></span>
<span data-ttu-id="98364-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98364-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98364-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="98364-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="98364-114">Liste der Anforderungsheader Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="98364-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98364-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="98364-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="98364-116">Liste der Antwortheader Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="98364-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98364-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98364-117">CommonParameters</span></span>
<span data-ttu-id="98364-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98364-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98364-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98364-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98364-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98364-120">INPUTS</span></span>

### <span data-ttu-id="98364-121">Keine</span><span class="sxs-lookup"><span data-stu-id="98364-121">None</span></span>

## <span data-ttu-id="98364-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98364-122">OUTPUTS</span></span>

### <span data-ttu-id="98364-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="98364-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="98364-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="98364-124">NOTES</span></span>

## <span data-ttu-id="98364-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98364-125">RELATED LINKS</span></span>

[<span data-ttu-id="98364-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98364-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98364-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98364-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98364-128">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98364-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98364-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98364-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98364-130">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98364-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98364-131">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="98364-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="98364-132">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="98364-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
