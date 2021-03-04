---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 63d90b646b639d7978dfbf734256976f423a3092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919496"
---
# <span data-ttu-id="9a726-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9a726-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="9a726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a726-102">SYNOPSIS</span></span>
<span data-ttu-id="9a726-103">Aktualisiert einen benutzerdefinierten Fehler in einem http-Listener eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9a726-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="9a726-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a726-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a726-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a726-105">DESCRIPTION</span></span>
<span data-ttu-id="9a726-106">Das **Cmdlet Set-AzApplicationGatewayCustomError** aktualisiert einen benutzerdefinierten Fehler in einem http-Listener eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9a726-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="9a726-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a726-107">EXAMPLES</span></span>

### <span data-ttu-id="9a726-108">Beispiel 1: Aktualisiert einen benutzerdefinierten Fehler eines Http-Listeners</span><span class="sxs-lookup"><span data-stu-id="9a726-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="9a726-109">Dieser Befehl aktualisiert den benutzerdefinierten Fehler von http-Statuscode 502 im http-Listener $listener 01 und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="9a726-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="9a726-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9a726-110">PARAMETERS</span></span>

### <span data-ttu-id="9a726-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="9a726-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="9a726-112">Url der Fehlerseite des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9a726-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9a726-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a726-113">-DefaultProfile</span></span>
<span data-ttu-id="9a726-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a726-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a726-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9a726-115">-HttpListener</span></span>
<span data-ttu-id="9a726-116">Der Http-Listener für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="9a726-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a726-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9a726-117">-StatusCode</span></span>
<span data-ttu-id="9a726-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9a726-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9a726-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a726-119">CommonParameters</span></span>
<span data-ttu-id="9a726-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a726-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a726-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a726-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a726-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a726-122">INPUTS</span></span>

### <span data-ttu-id="9a726-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9a726-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9a726-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a726-124">OUTPUTS</span></span>

### <span data-ttu-id="9a726-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9a726-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9a726-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9a726-126">NOTES</span></span>

## <span data-ttu-id="9a726-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9a726-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a726-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9a726-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9a726-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9a726-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9a726-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9a726-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
