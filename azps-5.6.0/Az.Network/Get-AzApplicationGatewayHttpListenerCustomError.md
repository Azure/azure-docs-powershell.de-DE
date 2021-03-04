---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944044"
---
# <span data-ttu-id="f2f6a-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2f6a-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f2f6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f6a-103">Ruft benutzerdefinierte Fehler von einem http-Listener eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="f2f6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2f6a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f6a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="f2f6a-106">Das **Get-AzApplicationGatewayCustomError-Cmdlet** ruft benutzerdefinierte Fehler von einem http-Listener eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="f2f6a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2f6a-107">EXAMPLES</span></span>

### <span data-ttu-id="f2f6a-108">Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Http-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="f2f6a-109">Dieser Befehl ruft den benutzerdefinierten Fehler von http-Statuscode 502 aus dem http-Listener-$listener 01 ab und gibt diesen zurück.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="f2f6a-110">Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Http-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="f2f6a-111">Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler aus dem http-Listener-$listener 01 ab und gibt sie zurück.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="f2f6a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f2f6a-112">PARAMETERS</span></span>

### <span data-ttu-id="f2f6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f6a-113">-DefaultProfile</span></span>
<span data-ttu-id="f2f6a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f6a-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f2f6a-115">-HttpListener</span></span>
<span data-ttu-id="f2f6a-116">Der Http-Listener für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f2f6a-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f2f6a-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f2f6a-117">-StatusCode</span></span>
<span data-ttu-id="f2f6a-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f2f6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f6a-119">CommonParameters</span></span>
<span data-ttu-id="f2f6a-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f6a-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2f6a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f6a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2f6a-122">INPUTS</span></span>

### <span data-ttu-id="f2f6a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2f6a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f2f6a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2f6a-124">OUTPUTS</span></span>

### <span data-ttu-id="f2f6a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f2f6a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f2f6a-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f2f6a-126">NOTES</span></span>

## <span data-ttu-id="f2f6a-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f2f6a-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2f6a-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2f6a-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f2f6a-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2f6a-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f2f6a-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2f6a-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
