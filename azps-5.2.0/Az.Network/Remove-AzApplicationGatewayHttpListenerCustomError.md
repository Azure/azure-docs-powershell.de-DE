---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299291"
---
# <span data-ttu-id="bd482-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bd482-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="bd482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd482-102">SYNOPSIS</span></span>
<span data-ttu-id="bd482-103">Entfernt einen benutzerdefinierten Fehler aus einem Http-Listener eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="bd482-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="bd482-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd482-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd482-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd482-105">DESCRIPTION</span></span>
<span data-ttu-id="bd482-106">Das **Cmdlet "Remove-AzApplicationGatewayCustomError"** entfernt einen benutzerdefinierten Fehler aus einem http-Listener eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="bd482-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="bd482-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd482-107">EXAMPLES</span></span>

### <span data-ttu-id="bd482-108">Beispiel 1: Entfernt einen benutzerdefinierten Fehler aus einem HTTP-Listener.</span><span class="sxs-lookup"><span data-stu-id="bd482-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="bd482-109">Dieser Befehl entfernt den benutzerdefinierten Fehler von http-Statuscode 502 aus dem http-Listener $listener 01 und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="bd482-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="bd482-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd482-110">PARAMETERS</span></span>

### <span data-ttu-id="bd482-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd482-111">-DefaultProfile</span></span>
<span data-ttu-id="bd482-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd482-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd482-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bd482-113">-HttpListener</span></span>
<span data-ttu-id="bd482-114">Der Http-Listener für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="bd482-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="bd482-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bd482-115">-StatusCode</span></span>
<span data-ttu-id="bd482-116">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="bd482-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bd482-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd482-117">CommonParameters</span></span>
<span data-ttu-id="bd482-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd482-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd482-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd482-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd482-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd482-120">INPUTS</span></span>

### <span data-ttu-id="bd482-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bd482-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bd482-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd482-122">OUTPUTS</span></span>

### <span data-ttu-id="bd482-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bd482-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bd482-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bd482-124">NOTES</span></span>

## <span data-ttu-id="bd482-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bd482-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd482-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bd482-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="bd482-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bd482-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="bd482-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bd482-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
