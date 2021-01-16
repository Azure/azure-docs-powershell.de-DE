---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290051"
---
# <span data-ttu-id="77f04-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77f04-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="77f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77f04-102">SYNOPSIS</span></span>
<span data-ttu-id="77f04-103">Aktualisiert einen benutzerdefinierten Fehler in einem Http-Listener eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="77f04-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="77f04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77f04-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77f04-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77f04-105">DESCRIPTION</span></span>
<span data-ttu-id="77f04-106">Das **Cmdlet "Set-AzApplicationGatewayCustomError"** aktualisiert einen benutzerdefinierten Fehler in einem http-Listener eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="77f04-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="77f04-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77f04-107">EXAMPLES</span></span>

### <span data-ttu-id="77f04-108">Beispiel 1: Aktualisiert einen benutzerdefinierten Fehler eines Http-Listeners.</span><span class="sxs-lookup"><span data-stu-id="77f04-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="77f04-109">Dieser Befehl aktualisiert den benutzerdefinierten Fehler des Http-Statuscodes 502 im http-Listener-$listener 01 und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="77f04-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="77f04-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77f04-110">PARAMETERS</span></span>

### <span data-ttu-id="77f04-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="77f04-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="77f04-112">Fehlerseiten-URL des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="77f04-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="77f04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f04-113">-DefaultProfile</span></span>
<span data-ttu-id="77f04-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77f04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f04-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="77f04-115">-HttpListener</span></span>
<span data-ttu-id="77f04-116">Der Http-Listener des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="77f04-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="77f04-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="77f04-117">-StatusCode</span></span>
<span data-ttu-id="77f04-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="77f04-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="77f04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f04-119">CommonParameters</span></span>
<span data-ttu-id="77f04-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f04-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f04-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f04-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77f04-122">INPUTS</span></span>

### <span data-ttu-id="77f04-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77f04-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="77f04-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77f04-124">OUTPUTS</span></span>

### <span data-ttu-id="77f04-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="77f04-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="77f04-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="77f04-126">NOTES</span></span>

## <span data-ttu-id="77f04-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="77f04-127">RELATED LINKS</span></span>

[<span data-ttu-id="77f04-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77f04-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="77f04-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77f04-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="77f04-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77f04-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
