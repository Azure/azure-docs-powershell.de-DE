---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f13591a92b52e00ed94e93fec480d810037f061d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660594"
---
# <span data-ttu-id="2c866-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2c866-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="2c866-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c866-102">SYNOPSIS</span></span>
<span data-ttu-id="2c866-103">Erstellt eine Rewrite-Regelaktion für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2c866-103">Creates a rewrite rule actionset for an application gateway.</span></span>

## <span data-ttu-id="2c866-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c866-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c866-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c866-105">DESCRIPTION</span></span>
<span data-ttu-id="2c866-106">**Das Cmdlet New-AzApplicationGatewayRewriteRuleActionSet** erstellt eine Rewrite-Regelaktion für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c866-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="2c866-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c866-107">EXAMPLES</span></span>

### <span data-ttu-id="2c866-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c866-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="2c866-109">Dieser Befehl erstellt eine Rewrite-Regelaktion und speichert das Ergebnis in der Variablen mit dem Namen $Action.</span><span class="sxs-lookup"><span data-stu-id="2c866-109">This command creates a rewrite rule actionset and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="2c866-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c866-110">PARAMETERS</span></span>

### <span data-ttu-id="2c866-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c866-111">-DefaultProfile</span></span>
<span data-ttu-id="2c866-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c866-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c866-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c866-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="2c866-114">Liste der Anforderungsheader Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="2c866-114">List of request header configurations</span></span>

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

### <span data-ttu-id="2c866-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c866-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="2c866-116">Liste der Antwortheader Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="2c866-116">List of response header configurations</span></span>

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

### <span data-ttu-id="2c866-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c866-117">CommonParameters</span></span>
<span data-ttu-id="2c866-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c866-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c866-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c866-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c866-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c866-120">INPUTS</span></span>

### <span data-ttu-id="2c866-121">Keine</span><span class="sxs-lookup"><span data-stu-id="2c866-121">None</span></span>

## <span data-ttu-id="2c866-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c866-122">OUTPUTS</span></span>

### <span data-ttu-id="2c866-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2c866-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="2c866-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c866-124">NOTES</span></span>

## <span data-ttu-id="2c866-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c866-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c866-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c866-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2c866-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c866-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2c866-128">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c866-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2c866-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c866-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2c866-130">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c866-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2c866-131">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2c866-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2c866-132">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c866-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
