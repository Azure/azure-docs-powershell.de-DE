---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: 6d5bbd0cd0b5581e129e63e7559c09751d8f91cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921011"
---
# <span data-ttu-id="5756d-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5756d-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="5756d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5756d-102">SYNOPSIS</span></span>
<span data-ttu-id="5756d-103">Erstellt eine Neuschreibung der Regelkopfkonfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5756d-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="5756d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5756d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5756d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5756d-105">DESCRIPTION</span></span>
<span data-ttu-id="5756d-106">**Das AzApplicationGatewayRewriteRuleHeaderConfiguration-Cmdlet** erstellt einen Umschreibregelaktionssatz für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5756d-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="5756d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5756d-107">EXAMPLES</span></span>

### <span data-ttu-id="5756d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5756d-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="5756d-109">Mit diesem Befehl wird eine Neuschreibregelkopfkonfiguration erstellt und das Ergebnis in der Variablen namens $hc.</span><span class="sxs-lookup"><span data-stu-id="5756d-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="5756d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5756d-110">PARAMETERS</span></span>

### <span data-ttu-id="5756d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5756d-111">-DefaultProfile</span></span>
<span data-ttu-id="5756d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5756d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5756d-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="5756d-113">-HeaderName</span></span>
<span data-ttu-id="5756d-114">Name der neu zu schreibende Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="5756d-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="5756d-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="5756d-115">-HeaderValue</span></span>
<span data-ttu-id="5756d-116">Kopfzeilenwert bis zum Satz für den angegebenen Kopfzeilennamen.</span><span class="sxs-lookup"><span data-stu-id="5756d-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="5756d-117">Die Kopfzeile wird gelöscht, wenn dies nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="5756d-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5756d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5756d-118">CommonParameters</span></span>
<span data-ttu-id="5756d-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5756d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5756d-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5756d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5756d-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5756d-121">INPUTS</span></span>

### <span data-ttu-id="5756d-122">Keine</span><span class="sxs-lookup"><span data-stu-id="5756d-122">None</span></span>

## <span data-ttu-id="5756d-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5756d-123">OUTPUTS</span></span>

### <span data-ttu-id="5756d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5756d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="5756d-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5756d-125">NOTES</span></span>

## <span data-ttu-id="5756d-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5756d-126">RELATED LINKS</span></span>

[<span data-ttu-id="5756d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5756d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5756d-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5756d-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5756d-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5756d-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5756d-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5756d-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5756d-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5756d-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5756d-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5756d-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="5756d-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5756d-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
