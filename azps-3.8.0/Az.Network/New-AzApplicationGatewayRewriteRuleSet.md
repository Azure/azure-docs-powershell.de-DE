---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004980"
---
# <span data-ttu-id="05a53-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="05a53-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05a53-102">SYNOPSIS</span></span>
<span data-ttu-id="05a53-103">Erstellt eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="05a53-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="05a53-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05a53-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05a53-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05a53-105">DESCRIPTION</span></span>
<span data-ttu-id="05a53-106">**Das Cmdlet "New-AzApplicationGatewayRewriteRuleSet"** erstellt eine Rewrite-Regelgruppe für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="05a53-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="05a53-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05a53-107">EXAMPLES</span></span>

### <span data-ttu-id="05a53-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05a53-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="05a53-109">Mit diesem Befehl wird eine Rewrite-Regelgruppe mit dem Namen ruleset1 erstellt und das Ergebnis in der Variablen mit dem Namen $RuleSet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="05a53-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="05a53-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05a53-110">PARAMETERS</span></span>

### <span data-ttu-id="05a53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a53-111">-DefaultProfile</span></span>
<span data-ttu-id="05a53-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05a53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05a53-113">-Name</span><span class="sxs-lookup"><span data-stu-id="05a53-113">-Name</span></span>
<span data-ttu-id="05a53-114">Der Name des RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="05a53-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="05a53-115">-RewriteRule</span></span>
<span data-ttu-id="05a53-116">Liste der Regeln zum Umschreiben</span><span class="sxs-lookup"><span data-stu-id="05a53-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="05a53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a53-117">CommonParameters</span></span>
<span data-ttu-id="05a53-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a53-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a53-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a53-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05a53-120">INPUTS</span></span>

### <span data-ttu-id="05a53-121">Keine</span><span class="sxs-lookup"><span data-stu-id="05a53-121">None</span></span>

## <span data-ttu-id="05a53-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05a53-122">OUTPUTS</span></span>

### <span data-ttu-id="05a53-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="05a53-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="05a53-124">NOTES</span></span>

## <span data-ttu-id="05a53-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05a53-125">RELATED LINKS</span></span>

[<span data-ttu-id="05a53-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="05a53-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="05a53-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="05a53-129">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05a53-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="05a53-130">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="05a53-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="05a53-131">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="05a53-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="05a53-132">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="05a53-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
