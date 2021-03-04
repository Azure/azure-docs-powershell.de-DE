---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ac18c96353e247c721f95acf83e174e18a578b2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938579"
---
# <span data-ttu-id="614ff-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="614ff-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="614ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="614ff-102">SYNOPSIS</span></span>
<span data-ttu-id="614ff-103">Entfernt eine Anforderungsroutingregel aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="614ff-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="614ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="614ff-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="614ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="614ff-105">DESCRIPTION</span></span>
<span data-ttu-id="614ff-106">Das **Cmdlet Remove-AzApplicationGatewayRequestRoutingRule** entfernt eine Anforderungsroutingregel aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="614ff-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="614ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="614ff-107">EXAMPLES</span></span>

### <span data-ttu-id="614ff-108">Beispiel 1: Entfernen einer Anforderungsroutingregel aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="614ff-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="614ff-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="614ff-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="614ff-110">Mit dem zweiten Befehl wird die Anforderungsroutingregel mit dem Namen Regel02 aus dem anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="614ff-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="614ff-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="614ff-111">PARAMETERS</span></span>

### <span data-ttu-id="614ff-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="614ff-112">-ApplicationGateway</span></span>
<span data-ttu-id="614ff-113">Gibt das Anwendungsgateway an, aus dem eine Anforderungsroutingregel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="614ff-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="614ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614ff-114">-DefaultProfile</span></span>
<span data-ttu-id="614ff-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="614ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="614ff-116">-Name</span><span class="sxs-lookup"><span data-stu-id="614ff-116">-Name</span></span>
<span data-ttu-id="614ff-117">Gibt den Namen der Anforderungsroutingregel an, für die dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="614ff-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="614ff-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614ff-118">CommonParameters</span></span>
<span data-ttu-id="614ff-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614ff-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614ff-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614ff-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614ff-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="614ff-121">INPUTS</span></span>

### <span data-ttu-id="614ff-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="614ff-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="614ff-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="614ff-123">OUTPUTS</span></span>

### <span data-ttu-id="614ff-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="614ff-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="614ff-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="614ff-125">NOTES</span></span>

## <span data-ttu-id="614ff-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="614ff-126">RELATED LINKS</span></span>

[<span data-ttu-id="614ff-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="614ff-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="614ff-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="614ff-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="614ff-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="614ff-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="614ff-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="614ff-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


