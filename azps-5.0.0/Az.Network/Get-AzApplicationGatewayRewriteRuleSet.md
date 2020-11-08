---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180190"
---
# <span data-ttu-id="dba88-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="dba88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dba88-102">SYNOPSIS</span></span>
<span data-ttu-id="dba88-103">Ruft den Rewrite-Regelsatz eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="dba88-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="dba88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dba88-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dba88-105">DESCRIPTION</span></span>
<span data-ttu-id="dba88-106">Ruft den Rewrite-Regelsatz eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="dba88-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="dba88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dba88-107">EXAMPLES</span></span>

### <span data-ttu-id="dba88-108">Beispiel 1: Abrufen einer bestimmten Regelgruppe zum Neuschreiben</span><span class="sxs-lookup"><span data-stu-id="dba88-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="dba88-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="dba88-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="dba88-110">Der zweite Befehl ruft die Rewrite-Regelgruppe mit dem Namen RuleSet01 aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="dba88-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="dba88-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dba88-111">PARAMETERS</span></span>

### <span data-ttu-id="dba88-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba88-112">-ApplicationGateway</span></span>
<span data-ttu-id="dba88-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba88-113">The applicationGateway</span></span>

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

### <span data-ttu-id="dba88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba88-114">-DefaultProfile</span></span>
<span data-ttu-id="dba88-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dba88-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba88-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dba88-116">-Name</span></span>
<span data-ttu-id="dba88-117">Der Name des Anwendungsgateway-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="dba88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba88-118">CommonParameters</span></span>
<span data-ttu-id="dba88-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba88-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dba88-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba88-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dba88-121">INPUTS</span></span>

### <span data-ttu-id="dba88-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba88-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dba88-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dba88-123">OUTPUTS</span></span>

### <span data-ttu-id="dba88-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="dba88-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="dba88-125">NOTES</span></span>

## <span data-ttu-id="dba88-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dba88-126">RELATED LINKS</span></span>

[<span data-ttu-id="dba88-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="dba88-128">Neu – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="dba88-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="dba88-130">Satz-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dba88-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="dba88-131">Neu – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="dba88-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="dba88-132">Neu – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dba88-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="dba88-133">Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="dba88-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
