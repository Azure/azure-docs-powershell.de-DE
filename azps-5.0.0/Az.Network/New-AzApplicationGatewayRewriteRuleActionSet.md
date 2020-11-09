---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302762"
---
# <span data-ttu-id="8fefe-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="8fefe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fefe-102">SYNOPSIS</span></span>
<span data-ttu-id="8fefe-103">Erstellt eine Regelaktion zum Umschreiben für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8fefe-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="8fefe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fefe-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fefe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fefe-105">DESCRIPTION</span></span>
<span data-ttu-id="8fefe-106">Mit **dem Cmdlet "New-AzApplicationGatewayRewriteRuleActionSet"** wird ein Rewrite-Regel Aktionssatz für ein Azure Application-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fefe-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="8fefe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fefe-107">EXAMPLES</span></span>

### <span data-ttu-id="8fefe-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fefe-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="8fefe-109">Mit diesem Befehl wird eine Rewrite-Regelaktion-Gruppe erstellt, und das Ergebnis wird in der Variablen mit dem Namen $Action gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8fefe-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="8fefe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fefe-110">PARAMETERS</span></span>

### <span data-ttu-id="8fefe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fefe-111">-DefaultProfile</span></span>
<span data-ttu-id="8fefe-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fefe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fefe-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fefe-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="8fefe-114">Liste der Anforderungsheader Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8fefe-114">List of request header configurations</span></span>

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

### <span data-ttu-id="8fefe-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fefe-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="8fefe-116">Liste der Antwortheader Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8fefe-116">List of response header configurations</span></span>

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

### <span data-ttu-id="8fefe-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fefe-117">-UrlConfiguration</span></span>
<span data-ttu-id="8fefe-118">URL-Konfiguration für Aktionssatz</span><span class="sxs-lookup"><span data-stu-id="8fefe-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fefe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fefe-119">CommonParameters</span></span>
<span data-ttu-id="8fefe-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fefe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fefe-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fefe-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fefe-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fefe-122">INPUTS</span></span>

### <span data-ttu-id="8fefe-123">Keine</span><span class="sxs-lookup"><span data-stu-id="8fefe-123">None</span></span>

## <span data-ttu-id="8fefe-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fefe-124">OUTPUTS</span></span>

### <span data-ttu-id="8fefe-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="8fefe-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fefe-126">NOTES</span></span>

## <span data-ttu-id="8fefe-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fefe-127">RELATED LINKS</span></span>

[<span data-ttu-id="8fefe-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8fefe-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8fefe-130">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8fefe-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8fefe-132">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fefe-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8fefe-133">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8fefe-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8fefe-134">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fefe-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="8fefe-135">Neu – AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fefe-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)