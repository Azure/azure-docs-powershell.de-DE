---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359790"
---
# <span data-ttu-id="aa593-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="aa593-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="aa593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa593-102">SYNOPSIS</span></span>
<span data-ttu-id="aa593-103">Fügt einem Http-Listener eines Anwendungsgateways einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="aa593-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="aa593-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa593-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa593-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa593-105">DESCRIPTION</span></span>
<span data-ttu-id="aa593-106">Das **Cmdlet "Add-AzApplicationGatewayCustomError"** fügt einem Http-Listener eines Anwendungsgateways einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="aa593-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="aa593-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa593-107">EXAMPLES</span></span>

### <span data-ttu-id="aa593-108">Beispiel 1: Fügt der Http-Listener-Ebene einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="aa593-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="aa593-109">Dieser Befehl fügt dem http-Listener-$listener 01 einen benutzerdefinierten Fehler mit dem Http-Statuscode 502 hinzu und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="aa593-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="aa593-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa593-110">PARAMETERS</span></span>

### <span data-ttu-id="aa593-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="aa593-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="aa593-112">Fehlerseiten-URL des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="aa593-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="aa593-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa593-113">-DefaultProfile</span></span>
<span data-ttu-id="aa593-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa593-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa593-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="aa593-115">-HttpListener</span></span>
<span data-ttu-id="aa593-116">Der Http-Listener für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="aa593-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="aa593-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="aa593-117">-StatusCode</span></span>
<span data-ttu-id="aa593-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="aa593-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="aa593-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa593-119">CommonParameters</span></span>
<span data-ttu-id="aa593-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa593-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa593-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa593-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa593-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa593-122">INPUTS</span></span>

### <span data-ttu-id="aa593-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aa593-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="aa593-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa593-124">OUTPUTS</span></span>

### <span data-ttu-id="aa593-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="aa593-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="aa593-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aa593-126">NOTES</span></span>

## <span data-ttu-id="aa593-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aa593-127">RELATED LINKS</span></span>

[<span data-ttu-id="aa593-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="aa593-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="aa593-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="aa593-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="aa593-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="aa593-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
