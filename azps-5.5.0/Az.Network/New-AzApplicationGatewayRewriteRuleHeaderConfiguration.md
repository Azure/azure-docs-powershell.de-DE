---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169878"
---
# <span data-ttu-id="40fba-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="40fba-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="40fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40fba-102">SYNOPSIS</span></span>
<span data-ttu-id="40fba-103">Erstellt eine Neuschreibung der Regelheaderkonfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="40fba-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="40fba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40fba-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40fba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40fba-105">DESCRIPTION</span></span>
<span data-ttu-id="40fba-106">**Das Cmdlet "AzApplicationGatewayRewriteRuleHeaderConfiguration"** erstellt einen Aktionssatz "Neuschreibungsregel" für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="40fba-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="40fba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40fba-107">EXAMPLES</span></span>

### <span data-ttu-id="40fba-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40fba-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="40fba-109">Dieser Befehl erstellt eine Neuschreibung der Regelheaderkonfiguration und speichert das Ergebnis in der Variablen namens $hc.</span><span class="sxs-lookup"><span data-stu-id="40fba-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="40fba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40fba-110">PARAMETERS</span></span>

### <span data-ttu-id="40fba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fba-111">-DefaultProfile</span></span>
<span data-ttu-id="40fba-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40fba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40fba-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="40fba-113">-HeaderName</span></span>
<span data-ttu-id="40fba-114">Name der neu zu schreibende Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="40fba-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="40fba-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="40fba-115">-HeaderValue</span></span>
<span data-ttu-id="40fba-116">Headerwert an den Satz für den angegebenen Headernamen.</span><span class="sxs-lookup"><span data-stu-id="40fba-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="40fba-117">Die Kopfzeile wird gelöscht, wenn diese nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="40fba-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="40fba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fba-118">CommonParameters</span></span>
<span data-ttu-id="40fba-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40fba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fba-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fba-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40fba-121">INPUTS</span></span>

### <span data-ttu-id="40fba-122">Keine</span><span class="sxs-lookup"><span data-stu-id="40fba-122">None</span></span>

## <span data-ttu-id="40fba-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40fba-123">OUTPUTS</span></span>

### <span data-ttu-id="40fba-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="40fba-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="40fba-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40fba-125">NOTES</span></span>

## <span data-ttu-id="40fba-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40fba-126">RELATED LINKS</span></span>

[<span data-ttu-id="40fba-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40fba-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="40fba-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40fba-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="40fba-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40fba-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="40fba-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40fba-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="40fba-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="40fba-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="40fba-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="40fba-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="40fba-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="40fba-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
