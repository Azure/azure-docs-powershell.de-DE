---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379362"
---
# <span data-ttu-id="589a7-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="589a7-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="589a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="589a7-102">SYNOPSIS</span></span>
<span data-ttu-id="589a7-103">Erstellt einen Regelaktionssatz "Neu schreiben" für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="589a7-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="589a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="589a7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="589a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="589a7-105">DESCRIPTION</span></span>
<span data-ttu-id="589a7-106">**Das Cmdlet "New-AzApplicationGatewayRewriteRuleActionSet"** erstellt einen Aktionssatz "Neuschreibungsregel" für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="589a7-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="589a7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="589a7-107">EXAMPLES</span></span>

### <span data-ttu-id="589a7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="589a7-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="589a7-109">Mit diesem Befehl wird ein Neuschreibregelaktionssatz erstellt und das Ergebnis in der Variablen namens "$action.</span><span class="sxs-lookup"><span data-stu-id="589a7-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="589a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="589a7-110">PARAMETERS</span></span>

### <span data-ttu-id="589a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589a7-111">-DefaultProfile</span></span>
<span data-ttu-id="589a7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="589a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="589a7-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="589a7-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="589a7-114">Liste der Konfigurationen von Anforderungsheadern</span><span class="sxs-lookup"><span data-stu-id="589a7-114">List of request header configurations</span></span>

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

### <span data-ttu-id="589a7-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="589a7-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="589a7-116">Liste der Konfigurationen von Antwortheadern</span><span class="sxs-lookup"><span data-stu-id="589a7-116">List of response header configurations</span></span>

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

### <span data-ttu-id="589a7-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="589a7-117">-UrlConfiguration</span></span>
<span data-ttu-id="589a7-118">URL Configuration for action set</span><span class="sxs-lookup"><span data-stu-id="589a7-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="589a7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589a7-119">CommonParameters</span></span>
<span data-ttu-id="589a7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="589a7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589a7-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589a7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589a7-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="589a7-122">INPUTS</span></span>

### <span data-ttu-id="589a7-123">Keine</span><span class="sxs-lookup"><span data-stu-id="589a7-123">None</span></span>

## <span data-ttu-id="589a7-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="589a7-124">OUTPUTS</span></span>

### <span data-ttu-id="589a7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="589a7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="589a7-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="589a7-126">NOTES</span></span>

## <span data-ttu-id="589a7-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="589a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="589a7-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589a7-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="589a7-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589a7-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="589a7-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589a7-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="589a7-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589a7-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="589a7-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="589a7-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="589a7-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="589a7-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="589a7-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="589a7-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="589a7-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="589a7-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)