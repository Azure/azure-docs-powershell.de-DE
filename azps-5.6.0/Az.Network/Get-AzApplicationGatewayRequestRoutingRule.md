---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 04c7ef7dd041ce26802f23117edab79353816283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940347"
---
# <span data-ttu-id="6bb49-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bb49-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6bb49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb49-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb49-103">Ruft die Anforderungsroutingregel eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="6bb49-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="6bb49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bb49-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bb49-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bb49-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb49-106">Das **Cmdlet Get-AzApplicationGatewayRequestRoutingRule** ruft die Anforderungsroutingregel eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="6bb49-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="6bb49-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bb49-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb49-108">Beispiel 1: Anfordern einer bestimmten Anforderungsroutingregel</span><span class="sxs-lookup"><span data-stu-id="6bb49-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6bb49-109">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6bb49-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6bb49-110">Der zweite Befehl ruft die Anforderungsroutingregel mit dem Namen Regel01 aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6bb49-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="6bb49-111">Beispiel 2: Anfordern einer Liste mit Anforderungsroutingregeln</span><span class="sxs-lookup"><span data-stu-id="6bb49-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="6bb49-112">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6bb49-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6bb49-113">Der zweite Befehl ruft eine Liste der Anforderungsroutingregeln aus dem Anwendungsgateway ab, die in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6bb49-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="6bb49-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6bb49-114">PARAMETERS</span></span>

### <span data-ttu-id="6bb49-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bb49-115">-ApplicationGateway</span></span>
<span data-ttu-id="6bb49-116">Gibt das Anwendungsgatewayobjekt an, das die Anforderungsroutingregel enthält.</span><span class="sxs-lookup"><span data-stu-id="6bb49-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="6bb49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb49-117">-DefaultProfile</span></span>
<span data-ttu-id="6bb49-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bb49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bb49-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6bb49-119">-Name</span></span>
<span data-ttu-id="6bb49-120">Gibt den Namen der Anforderungsroutingregel an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6bb49-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="6bb49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb49-121">CommonParameters</span></span>
<span data-ttu-id="6bb49-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb49-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bb49-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb49-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bb49-124">INPUTS</span></span>

### <span data-ttu-id="6bb49-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bb49-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bb49-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bb49-126">OUTPUTS</span></span>

### <span data-ttu-id="6bb49-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bb49-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6bb49-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6bb49-128">NOTES</span></span>

## <span data-ttu-id="6bb49-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6bb49-129">RELATED LINKS</span></span>

[<span data-ttu-id="6bb49-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bb49-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6bb49-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bb49-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6bb49-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bb49-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6bb49-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bb49-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


