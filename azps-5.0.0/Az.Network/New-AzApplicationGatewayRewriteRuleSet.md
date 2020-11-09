---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302761"
---
# <span data-ttu-id="37107-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="37107-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37107-102">SYNOPSIS</span></span>
<span data-ttu-id="37107-103">Erstellt eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="37107-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="37107-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37107-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37107-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37107-105">DESCRIPTION</span></span>
<span data-ttu-id="37107-106">**Das Cmdlet "New-AzApplicationGatewayRewriteRuleSet"** erstellt eine Rewrite-Regelgruppe für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="37107-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="37107-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37107-107">EXAMPLES</span></span>

### <span data-ttu-id="37107-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37107-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="37107-109">Mit diesem Befehl wird eine Rewrite-Regelgruppe mit dem Namen ruleset1 erstellt und das Ergebnis in der Variablen mit dem Namen $RuleSet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="37107-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="37107-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37107-110">PARAMETERS</span></span>

### <span data-ttu-id="37107-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37107-111">-DefaultProfile</span></span>
<span data-ttu-id="37107-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37107-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37107-113">-Name</span><span class="sxs-lookup"><span data-stu-id="37107-113">-Name</span></span>
<span data-ttu-id="37107-114">Der Name des RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="37107-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="37107-115">-RewriteRule</span></span>
<span data-ttu-id="37107-116">Liste der Regeln zum Umschreiben</span><span class="sxs-lookup"><span data-stu-id="37107-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="37107-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37107-117">CommonParameters</span></span>
<span data-ttu-id="37107-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37107-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37107-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37107-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37107-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37107-120">INPUTS</span></span>

### <span data-ttu-id="37107-121">Keine</span><span class="sxs-lookup"><span data-stu-id="37107-121">None</span></span>

## <span data-ttu-id="37107-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37107-122">OUTPUTS</span></span>

### <span data-ttu-id="37107-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="37107-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="37107-124">NOTES</span></span>

## <span data-ttu-id="37107-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37107-125">RELATED LINKS</span></span>

[<span data-ttu-id="37107-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37107-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37107-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37107-129">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37107-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37107-130">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="37107-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="37107-131">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37107-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="37107-132">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="37107-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
