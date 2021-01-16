---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305712"
---
# <span data-ttu-id="0f0b5-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f0b5-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0f0b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0b5-103">Ruft die Anforderungsroutingregel eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="0f0b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f0b5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f0b5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f0b5-105">DESCRIPTION</span></span>
<span data-ttu-id="0f0b5-106">Das **Cmdlet "Get-AzApplicationGatewayRequestRoutingRule"** ruft die Anforderungsroutingregel eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="0f0b5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f0b5-107">EXAMPLES</span></span>

### <span data-ttu-id="0f0b5-108">Beispiel 1: Anfordern einer bestimmten Anforderungsroutingregel</span><span class="sxs-lookup"><span data-stu-id="0f0b5-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="0f0b5-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0f0b5-110">Der zweite Befehl ruft die Anforderungsroutingregel mit dem Namen "Rule01" vom Anwendungsgateway ab, das in der Variablen namens "$AppGW.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="0f0b5-111">Beispiel 2: Anfordern einer Liste der Routingregeln für Anfragen</span><span class="sxs-lookup"><span data-stu-id="0f0b5-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="0f0b5-112">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0f0b5-113">Der zweite Befehl ruft eine Liste der Anforderungsroutingregeln aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="0f0b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f0b5-114">PARAMETERS</span></span>

### <span data-ttu-id="0f0b5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f0b5-115">-ApplicationGateway</span></span>
<span data-ttu-id="0f0b5-116">Gibt das Anwendungsgatewayobjekt an, das die Anforderungsroutingregel enthält.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="0f0b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0b5-117">-DefaultProfile</span></span>
<span data-ttu-id="0f0b5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0b5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0f0b5-119">-Name</span></span>
<span data-ttu-id="0f0b5-120">Gibt den Namen der Anforderungsroutingregel an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f0b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0b5-121">CommonParameters</span></span>
<span data-ttu-id="0f0b5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0b5-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f0b5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0b5-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f0b5-124">INPUTS</span></span>

### <span data-ttu-id="0f0b5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f0b5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0f0b5-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f0b5-126">OUTPUTS</span></span>

### <span data-ttu-id="0f0b5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f0b5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0f0b5-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f0b5-128">NOTES</span></span>

## <span data-ttu-id="0f0b5-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f0b5-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f0b5-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f0b5-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0f0b5-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f0b5-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0f0b5-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f0b5-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0f0b5-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f0b5-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


