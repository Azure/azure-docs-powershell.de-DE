---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004989"
---
# <span data-ttu-id="da4f0-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="da4f0-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="da4f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="da4f0-103">Erstellt eine Regel Header Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="da4f0-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="da4f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da4f0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da4f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="da4f0-106">**Das AzApplicationGatewayRewriteRuleHeaderConfiguration** -Cmdlet erstellt einen Rewrite-Regel Aktionssatz für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="da4f0-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="da4f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da4f0-107">EXAMPLES</span></span>

### <span data-ttu-id="da4f0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da4f0-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="da4f0-109">Mit diesem Befehl wird eine Rewrite-Regel Header-Konfiguration erstellt und das Ergebnis in der Variablen mit dem Namen $HC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="da4f0-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="da4f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="da4f0-110">PARAMETERS</span></span>

### <span data-ttu-id="da4f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4f0-111">-DefaultProfile</span></span>
<span data-ttu-id="da4f0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da4f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da4f0-113">-Headername</span><span class="sxs-lookup"><span data-stu-id="da4f0-113">-HeaderName</span></span>
<span data-ttu-id="da4f0-114">Name der Kopfzeile, die neu geschrieben werden soll</span><span class="sxs-lookup"><span data-stu-id="da4f0-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="da4f0-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="da4f0-115">-HeaderValue</span></span>
<span data-ttu-id="da4f0-116">Der Headerwert für den Satz für den angegebenen Headernamen.</span><span class="sxs-lookup"><span data-stu-id="da4f0-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="da4f0-117">Die Kopfzeile wird gelöscht, wenn diese ausgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="da4f0-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="da4f0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4f0-118">CommonParameters</span></span>
<span data-ttu-id="da4f0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da4f0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4f0-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4f0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4f0-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da4f0-121">INPUTS</span></span>

### <span data-ttu-id="da4f0-122">Keine</span><span class="sxs-lookup"><span data-stu-id="da4f0-122">None</span></span>

## <span data-ttu-id="da4f0-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da4f0-123">OUTPUTS</span></span>

### <span data-ttu-id="da4f0-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="da4f0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="da4f0-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="da4f0-125">NOTES</span></span>

## <span data-ttu-id="da4f0-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da4f0-126">RELATED LINKS</span></span>

[<span data-ttu-id="da4f0-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f0-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="da4f0-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f0-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="da4f0-129">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f0-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="da4f0-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f0-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="da4f0-131">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f0-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="da4f0-132">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="da4f0-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="da4f0-133">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="da4f0-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
