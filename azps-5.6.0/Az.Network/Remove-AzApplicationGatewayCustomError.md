---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 990c9624d949fa695b815a9530125a90693816ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918696"
---
# <span data-ttu-id="2f8c8-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2f8c8-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="2f8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8c8-103">Entfernt einen benutzerdefinierten Fehler aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="2f8c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f8c8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f8c8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="2f8c8-106">Das **Cmdlet Remove-AzApplicationGatewayCustomError** entfernt einen benutzerdefinierten Fehler aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="2f8c8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f8c8-107">EXAMPLES</span></span>

### <span data-ttu-id="2f8c8-108">Beispiel 1: Entfernt benutzerdefinierten Fehler aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="2f8c8-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="2f8c8-109">Mit diesem Befehl wird der benutzerdefinierte Fehler von http-Statuscode 502 aus dem Anwendungsgateway $appgw entfernt und das aktualisierte Gateway zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="2f8c8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2f8c8-110">PARAMETERS</span></span>

### <span data-ttu-id="2f8c8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f8c8-111">-ApplicationGateway</span></span>
<span data-ttu-id="2f8c8-112">Das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="2f8c8-112">The Application Gateway</span></span>

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

### <span data-ttu-id="2f8c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8c8-113">-DefaultProfile</span></span>
<span data-ttu-id="2f8c8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8c8-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="2f8c8-115">-StatusCode</span></span>
<span data-ttu-id="2f8c8-116">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="2f8c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8c8-117">CommonParameters</span></span>
<span data-ttu-id="2f8c8-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8c8-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f8c8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8c8-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f8c8-120">INPUTS</span></span>

### <span data-ttu-id="2f8c8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f8c8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f8c8-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f8c8-122">OUTPUTS</span></span>

### <span data-ttu-id="2f8c8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2f8c8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="2f8c8-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2f8c8-124">NOTES</span></span>

## <span data-ttu-id="2f8c8-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2f8c8-125">RELATED LINKS</span></span>

[<span data-ttu-id="2f8c8-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2f8c8-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="2f8c8-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2f8c8-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="2f8c8-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2f8c8-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="2f8c8-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2f8c8-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
